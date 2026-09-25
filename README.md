# Modelo Mobile

Editor web de diagramas entidade-relacionamento, pensado para celulares. Projeto independente inspirado no brModelo, sem vínculo com o aplicativo original.

## Recursos

- Entidades com atributos e atributos-chave.
- Relacionamentos normais e recursivos, com cardinalidades e papéis.
- Movimento por toque de entidades, atributos e cardinalidades.
- Posicionamento de novas entidades em espaços livres.
- Zoom com dois dedos, navegação pelo diagrama e enquadramento.
- Desfazer e refazer.
- Salvamento automático no navegador.
- Importação e exportação do modelo em JSON; exportação da imagem em SVG.

## Executar localmente

O projeto usa HTML, CSS e JavaScript, sem dependências de aplicação ou etapa de compilação.

Com Python 3 instalado, execute na pasta do projeto:

```sh
python -m http.server 8000
```

Abra http://localhost:8000 no navegador. Para hospedagem, publique os três arquivos da aplicação em um serviço de páginas estáticas com HTTPS.

## Arquivos

- `index.html`: estrutura da interface.
- `style.css`: estilos e adaptação para celular.
- `app.js`: edição, desenho, gestos, armazenamento e exportação.

## Uso

1. Adicione uma entidade e seus atributos.
2. Escolha **Rel. normal** para duas entidades ou **Rel. recursivo** para uma entidade com dois papéis.
3. Arraste elementos, atributos e cardinalidades para organizar o modelo.
4. Use o menu de três pontos para baixar uma cópia editável, exportar uma imagem ou abrir um modelo.

As posições manuais de atributos e cardinalidades são preservadas no JSON. A edição da entidade ou do relacionamento permite restaurar as posições automáticas.

## Armazenamento e limitações

Os diagramas ficam no armazenamento local do navegador e não são sincronizados entre dispositivos ou endereços. Excluir os dados do navegador também remove esses modelos. Baixe o JSON para manter uma cópia.

Esta versão trabalha com modelos conceituais. Não abre arquivos nativos `.brM` e não gera SQL. Os relacionamentos normais são binários. O limite atual por modelo é de 150 entidades, 300 relacionamentos e 30 atributos por entidade; importações aceitam arquivos de até 2 MB.

## Verificação

A versão exportada foi verificada em telas de celular e computador: criação e edição, relacionamentos recursivos, gestos de toque, posicionamento, desfazer/refazer, salvamento, importação JSON e exportação SVG.

