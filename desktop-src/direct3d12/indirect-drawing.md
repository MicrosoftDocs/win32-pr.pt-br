---
title: Desenho indireto
description: O desenho indireto permite que alguns atravessamentos de cena e de seleção sejam movidos da CPU para a GPU, o que pode melhorar o desempenho. O buffer de comando pode ser gerado pela CPU ou GPU.
ms.assetid: F8D6C88A-101E-4F66-999F-43206F6527B6
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55070bead6f848777cb81dd7fb33878ddcf7954a7f8a4fbb55f4ab9c01d4cea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123839"
---
# <a name="indirect-drawing"></a>Desenho indireto

O desenho indireto permite que alguns atravessamentos de cena e de seleção sejam movidos da CPU para a GPU, o que pode melhorar o desempenho. O buffer de comando pode ser gerado pela CPU ou GPU.

-   [Assinaturas de comando](#command-signatures)
-   [Estruturas de buffer de argumento indireto](#indirect-argument-buffer-structures)
-   [Criação de assinatura de comando](#command-signature-creation)
    -   [Nenhuma alteração de argumento](#no-argument-changes)
    -   [Constantes raiz e buffers de vértice](#root-constants-and-vertex-buffers)
-   [Tópicos relacionados](#related-topics)

## <a name="command-signatures"></a>Assinaturas de comando

O [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature)(objeto de assinatura de comando) permite que os aplicativos especifiquem o desenho indireto, em particular, a seguinte configuração:

-   O formato de buffer de argumento indireto.
-   O tipo de comando que será usado (dos métodos [**ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) [**DrawInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced), [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced)ou [**Dispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)).
-   O conjunto de associações de recursos que alterará a chamada por comando versus o conjunto que será herdado.

Na inicialização, um aplicativo cria um pequeno conjunto de **assinaturas de comando**. Em tempo de execução, o aplicativo preenche um buffer com comandos (por isso quer dizer que o desenvolvedor do aplicativo escolhe). Os comandos, opcionalmente, contêm o estado a ser definido para exibições de buffer de vértice, exibições de buffer de índice, constantes raiz e descritores de raiz (unraw ou Structured SRV/UAV/CBVs). Esses layouts de argumento não são específicos de hardware para que os aplicativos possam gerar os buffers diretamente. A assinatura de comando herda o estado restante da lista de comandos. Em seguida, o aplicativo chama [**ExecuteIndirect**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) para instruir a GPU a interpretar o conteúdo do buffer de argumento indireto de acordo com o formato definido por uma assinatura de comando específica.

Se a assinatura de comando alterar qualquer argumento raiz, ela será armazenada na assinatura de comando como um subconjunto de uma assinatura raiz.

Observe que nenhum estado de assinatura de comando vaza de volta para a lista de comandos quando a execução é concluída.

Por exemplo, suponha que um desenvolvedor de aplicativo queira que uma constante raiz exclusiva seja especificada por desenho de chamada no buffer de argumento indireto. O aplicativo criaria uma assinatura de comando que habilita o buffer de argumento indireto para especificar os seguintes parâmetros por chamada de desenho:

-   O valor de uma constante raiz.
-   Os argumentos Draw (contagem de vértices, contagem de instâncias, etc.)

O buffer de argumento indireto gerado pelo aplicativo deve conter uma matriz de registros de tamanho fixo. Cada estrutura corresponde a uma chamada de desenho. Cada estrutura contém os argumentos de desenho e o valor da constante raiz. O número de chamadas de desenho é especificado em um buffer visível de GPU separado.

Segue um exemplo de buffer de comando gerado pelo aplicativo:

![formato de buffer de comando](images/indirect-drawing-command-buffer.png)

## <a name="indirect-argument-buffer-structures"></a>Estruturas de buffer de argumento indireto

As estruturas a seguir definem como os argumentos específicos aparecem em um buffer de argumento indireto. Essas estruturas não aparecem em nenhuma API do D3D12. Os aplicativos usam essas definições ao gravar em um buffer de argumento indireto (com a CPU ou GPU):

-   [**\_Argumentos de desenho D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_arguments)
-   [**D3D12 \_ \_ argumentos indexados de desenho \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_draw_indexed_arguments)
-   [**\_Argumentos de expedição de D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_dispatch_arguments)
-   [**\_Exibição do \_ buffer de vértice D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_vertex_buffer_view)
-   [**\_Exibição do \_ buffer de índice D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_index_buffer_view)
-   \_Endereço virtual de GPU D3D12 \_ \_ (um sinônimo de typedef de UINT64).
-   [**\_Exibição de \_ buffer de constante D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_constant_buffer_view_desc)

## <a name="command-signature-creation"></a>Criação de assinatura de comando

Para criar uma assinatura de comando, use os seguintes itens de API:

-   [**ID3D12Device:: CreateCommandSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandsignature) (gera um [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature))
-   [**\_Tipo de \_ argumento INdireto D3D12 \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_indirect_argument_type)
-   [**\_Argumento indireto D3D12 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_indirect_argument_desc)
-   [**\_Desc de \_ assinatura de comando D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc)

A ordenação de argumentos em um buffer de argumento indireto é definida para corresponder exatamente à ordem dos argumentos especificados no parâmetro *pArguments* da [**assinatura de \_ comando D3D12 \_ \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_command_signature_desc). Todos os argumentos para uma chamada de/dispatch (computação) de desenho (gráfico) em um buffer de argumento indireto são totalmente empacotados. No entanto, os aplicativos têm permissão para especificar um stride de byte arbitrário entre os comandos de desenho/expedição em um buffer de argumento indireto.

A assinatura raiz deverá ser especificada se e somente se a assinatura de comando alterar um dos argumentos raiz.

Para a raiz SRV/UAV/CBV, o tamanho especificado do aplicativo é em bytes. A camada de depuração validará as seguintes restrições no endereço:

-   CBV – o endereço deve ser um múltiplo de 256 bytes.
-   O endereço bruto SRV/UAV – deve ser um múltiplo de 4 bytes.
-   SRV/UAV estruturado – o endereço deve ser um múltiplo da distância de byte da estrutura (declarado no sombreador).

Uma assinatura de comando específica é uma assinatura de comando de desenho ou de computação. Se uma assinatura de comando contiver uma operação de desenho, ela será uma assinatura de comando de gráficos. Caso contrário, a assinatura de comando deve conter uma operação de expedição e é uma assinatura de comando de computação.

As seções a seguir mostram alguns exemplos de assinaturas de comando.

### <a name="no-argument-changes"></a>Nenhuma alteração de argumento

Neste exemplo, o buffer de argumento indireto gerado pelo aplicativo contém uma matriz de estruturas de 36 bytes. Cada estrutura contém apenas os cinco parâmetros passados para [**DrawIndexedInstanced**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawindexedinstanced) (mais preenchimento).

O código para criar a descrição da assinatura de comando segue:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[1];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW_INDEXED;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 36;
ProgramDesc.NumArgumentDescs = 1;
ProgramDesc.pArguments = Args;
```

O layout de uma única estrutura dentro de um buffer de argumento indireto é:



| Bytes | Descrição           |
|-------|-----------------------|
| 0:3   | IndexCountPerInstance |
| 4:7   | InstanceCount         |
| 8:11  | StartIndexLocation    |
| 12:15 | BaseVertexLocation    |
| 16:19 | StartInstanceLocation |
| 20:35 | Preenchimento               |



 

### <a name="root-constants-and-vertex-buffers"></a>Constantes raiz e buffers de vértice

Neste exemplo, cada estrutura em um buffer de argumento indireto altera duas constantes raiz, altera uma associação de buffer de vértice e executa uma operação não indexada de desenho. Não há nenhum preenchimento entre as estruturas.

O código para criar a descrição da assinatura de comando é:

``` syntax
D3D12_INDIRECT_ARGUMENT_DESC Args[4];
Args[0].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[0].Constant.RootParameterIndex = 2;
Args[0].Constant.DestOffsetIn32BitValues = 0;
Args[0].Constant.Num32BitValuesToSet = 1;

Args[1].Type = D3D12_INDIRECT_ARGUMENT_TYPE_CONSTANT;
Args[1].Constant.RootParameterIndex = 6;
Args[1].Constant.DestOffsetIn32BitValues = 0;
Args[1].Constant.Num32BitValuesToSet = 1;

Args[2].Type = D3D12_INDIRECT_ARGUMENT_TYPE_VERTEX_BUFFER_VIEW;
Args[2].VertexBuffer.Slot = 3;

Args[3].Type = D3D12_INDIRECT_ARGUMENT_TYPE_DRAW;

D3D12_COMMAND_SIGNATURE_DESC ProgramDesc;
ProgramDesc.ByteStride = 40;
ProgramDesc.NumArgumentDescs = 4;
ProgramDesc.pArguments = Args;
```

O layout de uma única estrutura dentro do buffer de argumento indireto é o seguinte:



| Bytes | Descrição                               |
|-------|-------------------------------------------|
| 0:3   | Dados para o índice do parâmetro raiz 2           |
| 4:7   | Dados para o índice do parâmetro de raiz 6           |
| 8:15  | Endereço virtual do VB no slot 3 (64 bits)  |
| 16:19 | Tamanho do VB                                   |
| 20:23 | Stride do VB                                 |
| 24:27 | VertexCountPerInstance                    |
| 28:31 | InstanceCount                             |
| 32:35 | StartVertexLocation                       |
| 36:39 | StartInstanceLocation                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tutoriais de vídeo do DirectX Advanced Learning: executar a remoção de GPU indireta e assíncrona](https://www.youtube.com/watch?v=fKD-VKJeeds)
</dt> <dt>

[Remoção indireta de desenho e GPU: passo a passo de código](indirect-drawing-and-gpu-culling-.md)
</dt> <dt>

[Renderização](rendering.md)
</dt> </dl>

 

 
