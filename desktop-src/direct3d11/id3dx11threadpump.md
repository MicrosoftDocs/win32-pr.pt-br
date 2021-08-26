---
title: Interface ID3DX11ThreadPump (D3DX11core. h)
description: Uma bomba de thread executa tarefas de forma assíncrona.
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- Interface ID3DX11ThreadPump Direct3D 11
- Interface ID3DX11ThreadPump Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06f50e489503d02a6ea772be65678022dd36f6c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481282"
---
# <a name="id3dx11threadpump-interface"></a>Interface ID3DX11ThreadPump

> [!Note]  
> a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows.

 

Uma bomba de thread executa tarefas de forma assíncrona. Ele é criado chamando [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md). Há várias APIs que usam uma bomba de thread opcional como um parâmetro, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); Se você passar uma interface de bombeamento de thread para essas APIs, as funções serão executadas de forma assíncrona em um thread separado. Especialmente em máquinas com vários processadores, uma bomba de thread pode carregar recursos e processar dados sem uma diminuição perceptível no desempenho.

## <a name="members"></a>Membros

A interface **ID3DX11ThreadPump** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11ThreadPump** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX11ThreadPump** tem esses métodos.




| Método | Descrição | 
|--------|-------------|
| <a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a> | <blockquote>[!Note]<br />a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows.</blockquote><br /> Adiciona um item de trabalho à bomba do thread.<br /> | 
| <a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a> | <blockquote>[!Note]<br />a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows.</blockquote><br /> Obtém o número de itens em cada uma das três filas dentro da bomba do thread.<br /> | 
| <a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a> | <blockquote>[!Note]<br />a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows.</blockquote><br /> Obtém o número de itens de trabalho na bomba do thread.<br /> | 
| <a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a> | <blockquote>[!Note]<br />a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows.</blockquote><br /> Define itens de trabalho para o dispositivo depois que eles terminarem de carregar e processar.<br /> | 
| <a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a> | <blockquote>[!Note]<br />a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows.</blockquote><br /> Limpa todos os itens de trabalho da bomba de thread.<br /> | 
| <a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a> | <blockquote>[!Note]<br />a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida por Windows 8 e não tem suporte para aplicativos da loja Windows.</blockquote><br /> Aguarda a conclusão de todos os itens de trabalho na bomba do thread.<br /> | 




 

## <a name="remarks"></a>Comentários

### <a name="using-a-thread-pump"></a>Usando uma bomba de thread

A bomba de thread carrega e processa dados usando o seguinte processo de três etapas:

1.  Carregue e descompacte os dados com um [**carregador de dados**](id3dx11dataloader.md). O objeto data Loader tem três métodos que a bomba de thread chamará internamente, pois está carregando e descompactando os dados: [**ID3DX11DataLoader:: Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader::D ecompress**](id3dx11dataloader-decompress.md)e [**ID3DX11DataLoader::D estroy**](id3dx11dataloader-destroy.md). A funcionalidade específica dessas três APIs difere dependendo do tipo de dados que estão sendo carregados e descompactados. A interface do carregador de dados também pode ser herdada e suas APIs podem ser alteradas se uma estiver carregando um arquivo de dados definido em um formato personalizado próprio.
2.  Processe os dados com um [**processador de dados**](id3dx11dataprocessor.md). O objeto de processador de dados tem três métodos que a bomba de thread chamará internamente, pois está processando os dados: [**ID3DX11DataProcessor::P modelos**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor:: deviceobject**](id3dx11dataprocessor-createdeviceobject.md)e [**ID3DX11DataProcessor::D estroy**](id3dx11dataprocessor-destroy.md). A maneira como ele processa os dados será diferente dependendo do tipo de dados. Por exemplo, se os dados forem uma textura armazenada como JPEG, [**ID3DX11DataProcessor::P modelos**](id3dx11dataprocessor-process.md) fará a descompactação de JPEG para obter os bits de imagem bruta da imagem. Se os dados forem um sombreador, [**ID3DX11DataProcessor::P modelos**](id3dx11dataprocessor-process.md) compilará o HLSL em código de bytes. Depois que os dados forem processados, um objeto de dispositivo será criado para esses dados (com [**ID3DX11DataProcessor:: Createdeviceobject**](id3dx11dataprocessor-createdeviceobject.md)) e o objeto será adicionado a uma fila de objetos de dispositivo. A interface do processador de dados também pode ser herdada e suas APIs podem ser alteradas se um estiver processando um arquivo de dados definido em um formato personalizado próprio.
3.  Associe o objeto de dispositivo ao dispositivo. Isso é feito quando um aplicativo chama [**ID3DX11ThreadPump::P rocessdeviceworkitems**](id3dx11threadpump-processdeviceworkitems.md), que associará um número especificado de objetos na fila de objetos de dispositivo ao dispositivo.

A bomba de thread pode ser usada para carregar dados de uma das duas maneiras: chamando uma API que usa uma bomba de thread como um parâmetro, como [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) e [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), ou chamando [**ID3DX11ThreadPump:: AddWorkItem**](id3dx11threadpump-addworkitem.md). No caso das APIs que tomam uma bomba de thread, o carregador de dados e o processador de dados são criados internamente. No caso de AddWorkItem, o carregador de dados e o processador de dados devem ser criados com antecedência e, em seguida, passados para AddWorkItem. O D3DX11 fornece um conjunto de APIs para criar carregadores de dados e processadores de dados que têm funcionalidade para carregar e processar formatos de dados comuns. Para formatos de dados personalizados, as interfaces do carregador de dados e do processador de dados devem ser herdadas e seus métodos devem ser redefinidos.

O objeto de bomba de thread ocupa uma quantidade significativa de recursos, portanto, em geral, apenas um deve ser criado por aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                 |
| Cabeçalho<br/>                   | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

