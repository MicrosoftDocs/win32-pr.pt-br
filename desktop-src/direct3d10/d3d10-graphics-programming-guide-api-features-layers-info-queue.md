---
description: Personalizar a saída de depuração com ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Personalizar a saída de depuração com ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ac7dd34b19cfe1fc7835a2026ae2dd28b9dcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010226"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a>Personalizar a saída de depuração com ID3D10InfoQueue (Direct3D 10)

A fila de informações é gerenciada por uma interface (consulte a [**interface ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) que armazena, recupera e filtra mensagens de depuração. A fila consiste em: uma fila de mensagens, uma pilha de filtro de armazenamento opcional e uma pilha de filtro de recuperação opcional. A pilha de filtro de armazenamento pode ser usada para filtrar as mensagens que você deseja armazenar. a pilha de filtro de recuperação pode ser usada para filtrar as mensagens que você deseja armazenar. Depois de filtrar uma mensagem, a mensagem será impressa na janela de depuração e armazenada na pilha apropriada.

Em geral:

-   Chamar [**ID3D10InfoQueue:: AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) para gerar mensagens definidas pelo usuário
-   Call [**ID3D10InfoQueue:: GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) é usado para obter mensagens (que passam por um filtro de recuperação opcional).

## <a name="registry-controls"></a>Controles do registro

Use chaves do registro para ajustar as configurações de filtro, ajustar pontos de interrupção e ativar mudo da saída de depuração. A camada de depuração verificará esses caminhos para chaves do registro; o primeiro caminho encontrado será usado.

1.  HKCU \\ software \\ Microsoft \\ Direct3D \\<subchave definida pelo usuário>
2.  HKLM \\ software \\ Microsoft \\ Direct3D \\<subchave definida pelo usuário>
3.  HKCU \\ software \\ Microsoft \\ Direct3D

Em que:

-   O HKCU tem para HKEY \_ Current \_ User e HKLM para o \_ computador local hKey \_ .
-   <subchave definida pelo usuário> é um nome arbitrário para armazenar as configurações de depuração de um aplicativo

### <a name="filtering-debug-messages-using-registry-keys"></a>Filtrando mensagens de depuração usando chaves do registro

Se o registro contiver uma chave InfoQueueStorageFilterOverride (e for diferente de zero), as mensagens (e a saída de depuração) poderão ser filtradas adicionando os seguintes controles de registro.

-   Categoria sem som DWORD \_ \_ \* – depurar saída se essa chave for diferente de zero.
-   Severidade sem \_ som \_ \* de DWORD-a saída de depuração será desabilitada se essa chave for diferente de zero.
-   ID de mudo DWORD \_ \_ \* -o nome da mensagem ou o número pode ser usado para \* (assim como a ID de interrupção \_ \_ \* descrita anteriormente). A saída de depuração será desabilitada se essa chave for diferente de zero.
-   \_ \_ Informações de severidade de mudo de DWORD-a saída de depuração será habilitada se essa chave for diferente de zero. Por padrão, quando o InfoQueueStorageFilterOverride está habilitado, as mensagens de depuração com informações de severidade estão sem áudio-portanto, para essa chave, é possível que as informações sejam reativadas.

Esses controles alteram se uma mensagem é gravada ou exibida; Eles não afetam se uma API passa ou falha.

### <a name="setting-break-conditions-using-registry-keys"></a>Definindo condições de interrupção usando chaves do registro

Os aplicativos podem ser forçados a interromper uma mensagem usando as seguintes chaves do registro.

**EnableBreakOnMessage** -essa chave permite a interrupção de mensagens (e faz com que as configurações de SetBreakOnCategory ()/SetBreakOnSeverity ()/SetBreakOnID () sejam ignoradas). As mensagens reais a serem quebradas são definidas usando um ou mais valores de interrupção \_ \* definidos abaixo.

-   **Interrupção \_ \_Categoria \** _-quebra em qualquer mensagem passando pelos filtros de armazenamento. \_ é uma das mensagens de \_ categoria de mensagem d3d10 \_ .
-   **Interrupção \_ \_Severidade \** _-quebra em qualquer mensagem que passe pelos filtros de armazenamento. \_ é uma das mensagens de \_ severidade da mensagem d3d10 \_ \_ .
-   **Interrupção \_ \_ID \** _-break em qualquer mensagem que passe pelos filtros de armazenamento. \_ é uma das mensagens de \_ ID de mensagem d3d10 \_ \_ ou pode ser o valor numérico da enumeração Error. Por exemplo, suponha que a mensagem com a ID " \_ hipotética da ID da mensagem d3d10 \_ \_ " tivesse o valor 123 na \_ enumeração da ID da mensagem d3d10 \_ . Nesse caso, a criação da ID de interrupção de valor \_ \_ hipotética = 1 ou ID de \_ interrupção \_ 123 = 1 faria o mesmo intervalo quando uma mensagem com ID de mensagem d3d10 ID \_ \_ \_ hipotética for encontrada.

### <a name="muting-debug-output-using-registry-keys"></a>Saída de depuração de mudo usando chaves do registro

A saída de depuração pode ser mudo usando uma chave MuteDebugOutput. A presença desse valor no registro força a substituição do método [**ID3D10InfoQueue:: SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) do InfoQueue. MuteDebugOutput interrompe as mensagens que passam o filtro de armazenamento para serem enviadas para a saída de depuração.

## <a name="disabling-debug-layer-messages"></a>Desabilitando mensagens da camada de depuração

As mensagens da camada de depuração podem ser desabilitadas individualmente ou como um grupo em tempo de execução, especificando filtros usando [**ID3D10InfoQueue:: AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries). O argumento *pFilter* para **ID3D10InfoQueue:: AddStorageFilterEntries** usa uma estrutura de filtro da fila de informações de [**d3d10 \_ \_ \_**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) que contém uma lista de permissões e uma lista de negações. As listas permitir e negar são descritas por estruturas desc de filtro de [**d3d10 de \_ informações \_ \_ \_**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) que permitem que a filtragem seja especificada por catergory, severidade e ID de mensagem individual.

O código a seguir é um exemplo de configuração da [**interface ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) para negar a \_ mensagem ID de mensagem do d3d10 buffer de índice de desenho de \_ \_ dispositivo \_ \_ \_ \_ muito \_ pequeno.


```
  //retrieve the ID3D10InfoQueue from a Direct3D device created with the D3D10_CREATE_DEVICE_DEBUG flag
  ID3D10InfoQueue * pInfoQueue;
    g_pd3dDevice->QueryInterface( __uuidof(ID3D10InfoQueue),  (void **)&pInfoQueue );
    
  //set up the list of messages to filter
    D3D10_MESSAGE_ID messageIDs [] = { D3D10_MESSAGE_ID_DEVICE_DRAW_INDEX_BUFFER_TOO_SMALL };
    
  //set the DenyList to use the list of messages
    D3D10_INFO_QUEUE_FILTER filter = { 0 };
    filter.DenyList.NumIDs = 1;
    filter.DenyList.pIDList = messageIDs;
    
  //apply the filter to the info queue
    pInfoQueue->AddStorageFilterEntries( &filter );  
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Camadas de API](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[Recursos de API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



