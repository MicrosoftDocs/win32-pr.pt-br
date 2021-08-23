---
description: Personalizar a saída de depuração com ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Personalizar a saída de depuração com ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212b78352ccc9139c069ca5d388993fd83aca6833d77547a91401bc40380fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753826"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a>Personalizar a saída de depuração com ID3D10InfoQueue (Direct3D 10)

A fila de informações é gerenciada por uma interface (consulte [**Interface ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) que armazena, recupera e filtra mensagens de depuração. A fila consiste em: uma fila de mensagens, uma pilha de filtros de armazenamento opcional e uma pilha de filtros de recuperação opcional. A pilha de filtro de armazenamento pode ser usada para filtrar as mensagens que você deseja armazenar; A pilha de filtro de recuperação pode ser usada para filtrar as mensagens que você deseja armazenar. Depois de filtrar uma mensagem, a mensagem será impressa na janela de depuração e armazenada na pilha apropriada.

Em geral:

-   Chame [**ID3D10InfoQueue::AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) para gerar mensagens definidas pelo usuário
-   A [**chamada ID3D10InfoQueue::GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) é usada para obter mensagens (que passam por um filtro de recuperação opcional).

## <a name="registry-controls"></a>Controles do Registro

Use chaves do Registro para ajustar as configurações de filtro, ajustar pontos de quebra e para desativar a saída de depuração. A camada de depuração verificará esses caminhos para chaves do Registro; o primeiro caminho encontrado será usado.

1.  HKCU \\ Software \\ Microsoft \\ Direct3D \\<subkey definida pelo usuário>
2.  HKLM \\ Software \\ Microsoft \\ Direct3D \\<subkey definida pelo usuário>
3.  HKCU \\ Software \\ Microsoft \\ Direct3D

Em que:

-   HKCU é o HKEY \_ CURRENT \_ USER e HKLM é o HKEY \_ LOCAL \_ MACHINE.
-   <subkey definida pelo usuário> é um nome arbitrário para armazenar configurações de depuração para um aplicativo

### <a name="filtering-debug-messages-using-registry-keys"></a>Filtrando mensagens de depuração usando chaves do Registro

Se o Registro contiver uma chave InfoQueueStorageFilterOverride (e for não zero), as mensagens (e a saída de depuração) poderão ser filtradas adicionando os seguintes controles do Registro.

-   DWORD Mute \_ CATEGORY \_ \* – depure a saída se essa chave for não zero.
-   DWORD Mute SEVERITY – a saída \_ \_ \* de depuração será desabilitada se essa chave for não zero.
-   DWORD Mute ID – o nome ou o número da mensagem pode ser usado para (assim como para \_ \_ \* \* a ID de BreakOn \_ descrita \_ \* anteriormente). A saída de depuração será desabilitada se essa chave não for zero.
-   DWORD Informações de SEVERIDADE de Depuração – a saída \_ \_ de depuração será HABILITADA se essa chave for não zero. Por padrão, quando InfoQueueStorageFilterOverride está habilitado, as mensagens de depuração com INFORMAÇÕES de severidade são mudadas – portanto, para essa chave permite que INFO seja ativada novamente.

Esses controles alteram se uma mensagem é registrada ou exibida; eles não afetam se uma API é aprovada ou falha.

### <a name="setting-break-conditions-using-registry-keys"></a>Definindo condições de quebra usando chaves do Registro

Os aplicativos podem ser forçados a quebrar em uma mensagem usando as chaves do Registro a seguir.

**EnableBreakOnMessage** – essa chave permite a quebra de mensagens (e faz com que as configurações setBreakOnCategory()/SetBreakOnSeverity()/SetBreakOnID() de i sejam ignoradas). As mensagens reais para quebrar são definidas usando um ou mais valores BreakOn \_ \* definidos abaixo.

-   **BreakOn \_ \_CATEGORY \** _ – quebra em qualquer mensagem que passe pelos filtros de armazenamento. \_ é uma das mensagens D3D10 \_ MESSAGE \_ CATEGORY.
-   **BreakOn \_ SEVERITY \_ \** _ – quebra em qualquer mensagem que passe pelos filtros de armazenamento. \_ é uma das mensagens D3D10 \_ MESSAGE \_ \_ SEVERITY.
-   **BreakOn \_ ID \_ \** _ – quebra em qualquer mensagem que passe pelos filtros de armazenamento. \_ é uma das mensagens de ID da MENSAGEM D3D10 ou pode ser o valor numérico \_ \_ da \_ enumeração de erro. Por exemplo, suponha que a mensagem com a ID "D3D10 MESSAGE ID HYPOTHETICAL" tenha o valor \_ \_ \_ 123 na enumeração D3D10 \_ MESSAGE \_ ID. Nesse caso, criar o valor BreakOn \_ ID \_ HYPOTHETICAL=1 ou BreakOn ID 123=1 realizaria a mesma coisa – quebra quando uma mensagem com A \_ \_ ID D3D10 ID DE MENSAGEM \_ \_ HIPOTÉTICA é \_ encontrada.

### <a name="muting-debug-output-using-registry-keys"></a>Muting Debug Output using Registry Keys

A saída de depuração pode ser mudada usando uma chave MuteDebugOutput. A presença desse valor no Registro força a substituição do método [**ID3D10InfoQueue::SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) do InfoQueue. MuteDebugOutput impede que mensagens que passam pelo filtro de armazenamento são enviadas para a saída de depuração.

## <a name="disabling-debug-layer-messages"></a>Desabilitando mensagens da camada de depuração

As mensagens da camada de depuração podem ser desabilitadas individualmente ou como um grupo em runtime especificando filtros usando [**ID3D10InfoQueue::AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries). O *argumento pFilter* para **ID3D10InfoQueue::AddStorageFilterEntries** assume uma estrutura [**D3D10 \_ INFO QUEUE \_ \_ FILTER**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) que contém uma lista de permitir e uma lista de negação. As listas de permitir e negar são descritas pelas estruturas [**\_ \_ \_ \_ DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) FILTRO DE FILA DE INFORMAÇÕES D3D10 QUE permitem que a filtragem seja especificada por categoria, severidade e ID de mensagem individual.

O código a seguir é um exemplo de configuração da [**interface ID3D10InfoQueue**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) para negar a mensagem D3D10 \_ MESSAGE \_ ID DEVICE DRAW INDEX \_ BUFFER TOO \_ \_ \_ \_ \_ SMALL.


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

[Recursos da API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



