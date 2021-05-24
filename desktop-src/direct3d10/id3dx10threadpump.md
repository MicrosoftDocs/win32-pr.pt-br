---
description: Usado para executar tarefas de forma assíncrona e criado com D3DX10CreateThreadPump.
ms.assetid: 8d03c94a-9b64-464c-b0f4-4e5f5a00503f
title: Interface ID3DX10ThreadPump (D3DX10.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10ThreadPump
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aecab39b655998533c80f1fff56e3f10d941f551
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335650"
---
# <a name="id3dx10threadpump-interface"></a>Interface ID3DX10ThreadPump

Usado para executar tarefas de forma assíncrona e criado com [**D3DX10CreateThreadPump**](d3dx10createthreadpump.md). Há várias APIs D3DX10 que podem, opcionalmente, usar uma bomba de thread como um parâmetro, como [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**D3DX10CompileFromFile**](d3dx10compilefromfile.md) (consulte comentários para a lista completa). Se a bomba de thread for passada para essas APIs, elas serão executadas de forma assíncrona em um thread de bomba de thread separado. A vantagem de fazer isso é que ele pode fazer com que o carregamento e o processamento de grandes quantidades de dados ocorram sem ver uma lentidão notável no desempenho na tela.

## <a name="members"></a>Membros

A interface **ID3DX10ThreadPump** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10ThreadPump** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ID3DX10ThreadPump** tem esses métodos.



| Método                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddWorkItem**](id3dx10threadpump-addworkitem.md)                       | Adicione um item de trabalho à bomba de thread.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| [**GetQueueStatus**](id3dx10threadpump-getqueuestatus.md)                 | Obter o número de itens em cada uma das três filas dentro da bomba de thread.<br/>                                                                                                                                                                                                                                                                                                                                           |
| [**GetWorkItemCount**](id3dx10threadpump-getworkitemcount.md)             | Obter o número de itens de trabalho atualmente na bomba de thread.<br/>                                                                                                                                                                                                                                                                                                                                                            |
| [**ProcessDeviceWorkItems**](id3dx10threadpump-processdeviceworkitems.md) | De definir itens de trabalho para o dispositivo depois que eles terminarem de carregar e processar. Quando a bomba de thread terminar de carregar e processar um recurso ou sombreador, ela o manterá em uma fila até que essa API seja chamada, momento em que os itens processados serão definidos como o dispositivo. Isso é útil para controlar a quantidade de processamento gasto na associação de recursos ao dispositivo para cada quadro. Consulte Observações.<br/> |
| [**PurgeAllItems**](id3dx10threadpump-purgeallitems.md)                   | Limpar todos os itens de trabalho da bomba de thread.<br/>                                                                                                                                                                                                                                                                                                                                                                            |
| [**WaitForAllItems**](id3dx10threadpump-waitforallitems.md)               | Aguarde até que todos os itens de trabalho na bomba de thread sejam concluídos.<br/>                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Comentários

A bomba de thread carrega e processa dados em um processo de 3 etapas. Ele vai:

1.  Carregue e descompacte os dados com um carregador de dados. O objeto data Loader tem três métodos que a bomba de thread chamará internamente, pois está carregando e descompactando os dados: [**ID3DX10DataLoader:: Load**](id3dx10dataloader-load.md), [**ID3DX10DataLoader::D ecompress**](id3dx10dataloader-decompress.md)e [**ID3DX10DataLoader::D estroy**](id3dx10dataloader-destroy.md). A funcionalidade específica dessas três APIs difere dependendo do tipo de dados que estão sendo carregados e descompactados. A interface do carregador de dados também pode ser herdada e suas APIs podem ser alteradas se uma estiver carregando um arquivo de dados definido em um formato personalizado próprio.
2.  Processe os dados com um processador de dados. O objeto de processador de dados tem três métodos que a bomba de thread chamará internamente, pois está processando os dados: [**ID3DX10DataProcessor::P modelos**](id3dx10dataprocessor-process.md), [**ID3DX10DataProcessor:: deviceobject**](id3dx10dataprocessor-createdeviceobject.md)e [**ID3DX10DataProcessor::D estroy**](id3dx10dataprocessor-destroy.md). A maneira como ele processa os dados será diferente dependendo do tipo de dados. Por exemplo, se os dados forem uma textura armazenada como JPEG, **ID3DX10DataProcessor::P modelos** fará a descompactação de JPEG para obter os bits de imagem bruta da imagem. Se os dados forem um sombreador, **ID3DX10DataProcessor::P modelos** compilará o HLSL em código de bytes. Depois que os dados forem processados, um objeto de dispositivo será criado para esses dados (com **ID3DX10DataProcessor:: Createdeviceobject**) e o objeto será adicionado a uma fila de objetos de dispositivo. A interface do processador de dados também pode ser herdada e suas APIs podem ser alteradas se um estiver processando um arquivo de dados definido em um formato personalizado próprio.
3.  Associe o objeto de dispositivo ao dispositivo. Isso é feito quando o aplicativo chama [**ID3DX10ThreadPump::P rocessDeviceWorkItems**](id3dx10threadpump-processdeviceworkitems.md), que vinculará um número especificado de objetos na fila de objetos de dispositivo ao dispositivo.

A bomba de thread pode ser usada para carregar dados de uma das duas maneiras: chamando uma API que utiliza uma bomba de thread como um parâmetro, como [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) e [**D3DX10CompileFromFile**](d3dx10compilefromfile.md)ou chamando [**ID3DX10ThreadPump::AddWorkItem**](id3dx10threadpump-addworkitem.md). No caso das APIs que levam uma bomba de thread, o carregador de dados e o processador de dados são criados internamente. No caso de **AddWorkItem**, o carregador de dados e o processador de dados devem ser criados com antecedência e, em seguida, passados para AddWorkItem. O D3DX10 fornece um conjunto de APIs para criar carregadores de dados e processadores de dados que têm funcionalidade para carregar e processar formatos de dados comuns (consulte comentários para ver a lista completa de APIs). Para formatos de dados personalizados, as interfaces do carregador de dados e do processador de dados devem ser herdadas e seus métodos devem ser redefinidos.

O objeto de bomba de thread ocupa uma quantidade substancial de recursos, portanto, geralmente, apenas um deve ser criado por aplicativo.

Carregadores de dados D3DX10 integrados



|                                                                           |  Descrição                                        |
|----------------------------------------------------------------------------|------------------------------------------|
| [**D3DX10CreateAsyncFileLoader**](d3dx10createasyncfileloader.md)         | Crie um carregador de arquivos de forma assíncrona.     |
| [**D3DX10CreateAsyncMemoryLoader**](d3dx10createasyncmemoryloader.md)     | Crie um carregador de dados de forma assíncrona.     |
| [**D3DX10CreateAsyncResourceLoader**](d3dx10createasyncresourceloader.md) | Crie um carregador de recursos de forma assíncrona. |



 

Processadores de dados D3DX10 integrados



|                                                                                                 |  Descrição                                                                                                                                                  |
|--------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md)                   | Crie um processador de dados a ser usado com uma bomba de thread. Essa API é semelhante a D3DX10CreateAsyncTextureInfoProcessor, mas também carrega a textura. |
| [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md)           | Crie um processador de dados a ser usado com uma bomba de thread.                                                                                             |
| [**D3DX10CreateAsyncShaderCompilerProcessor**](d3dx10createasyncshadercompilerprocessor.md)     | Compile um sombreador e crie um processador de dados de forma assíncrona.                                                                                       |
| [**D3DX10CreateAsyncEffectCompilerProcessor**](d3dx10createasynceffectcompilerprocessor.md)     | Crie um efeito com um processador de dados de forma assíncrona.                                                                                             |
| [**D3DX10CreateAsyncEffectCreateProcessor**](d3dx10createasynceffectcreateprocessor.md)         | Crie um pool de efeitos de forma assíncrona.                                                                                                              |
| [**D3DX10CreateAsyncEffectPoolCreateProcessor**](d3dx10createasynceffectpoolcreateprocessor.md) | Crie um processador de dados de forma assíncrona.                                                                                                            |
| [**D3DX10CreateAsyncShaderPreprocessProcessor**](d3dx10createasyncshaderpreprocessprocessor.md) | Crie um processador de dados para um sombreador de forma assíncrona.                                                                                               |



 

APIs que usam uma bomba de thread como um parâmetro.



|                                                                                                 | Descrição                                                                 |
|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**D3DX10CompileFromFile**](d3dx10compilefromfile.md)                                           | Compilar um sombreador de um arquivo.                                    |
| [**D3DX10CompileFromMemory**](d3dx10compilefrommemory.md)                                       | Compile um sombreador que reside na memória.                             |
| [**D3DX10CompileFromResource**](d3dx10compilefromresource.md)                                   | Compilar um sombreador de um recurso.                                |
| [**D3DX10CreateEffectFromFile**](d3dx10createeffectfromfile.md)                                 | Crie um efeito de um arquivo.                                    |
| [**D3DX10CreateEffectFromMemory**](d3dx10createeffectfrommemory.md)                             | Crie um efeito da memória.                                    |
| [**D3DX10CreateEffectFromResource**](d3dx10createeffectfromresource.md)                         | Crie um efeito de um recurso.                                |
| [**D3DX10CreateEffectPoolFromFile**](d3dx10createeffectpoolfromfile.md)                         | Crie um pool de efeitos de um arquivo.                               |
| [**D3DX10CreateEffectPoolFromMemory**](d3dx10createeffectpoolfrommemory.md)                     | Crie um pool de efeitos de um arquivo que reside na memória.            |
| [**D3DX10CreateEffectPoolFromResource**](d3dx10createeffectpoolfromresource.md)                 | Crie um pool de efeitos de um recurso.                           |
| [**D3DX10PreprocessShaderFromFile**](d3dx10preprocessshaderfromfile.md)                         | Crie um sombreador de um arquivo sem compilá-lo.                |
| [**D3DX10PreprocessShaderFromMemory**](d3dx10preprocessshaderfrommemory.md)                     | Crie um sombreador de memória sem compilá-lo.                |
| [**D3DX10PreprocessShaderFromResource**](d3dx10preprocessshaderfromresource.md)                 | Crie um sombreador de um recurso sem compilá-lo.            |
| [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)         | Crie uma exibição sombreador-recurso de um arquivo.                       |
| [**D3DX10CreateShaderResourceViewFromMemory**](d3dx10createshaderresourceviewfrommemory.md)     | Crie uma exibição de recurso de sombreador de um arquivo na memória.             |
| [**D3DX10CreateShaderResourceViewFromResource**](d3dx10createshaderresourceviewfromresource.md) | Criar um sombreador – modo de exibição de recursos de um recurso.                   |
| [**D3DX10GetImageInfoFromFile**](d3dx10getimageinfofromfile.md)                                 | Recupera informações sobre um determinado arquivo de imagem.                  |
| [**D3DX10GetImageInfoFromMemory**](d3dx10getimageinfofrommemory.md)                             | Obtenha informações sobre uma imagem já carregada na memória.       |
| [**D3DX10GetImageInfoFromResource**](d3dx10getimageinfofromresource.md)                         | Recupera informações sobre uma determinada imagem em um recurso.         |
| [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)                               | Crie um recurso de textura a partir de um arquivo.                           |
| [**D3DX10CreateTextureFromMemory**](d3dx10createtexturefrommemory.md)                           | Crie um recurso de textura a partir de um arquivo que reside na memória do sistema. |
| [**D3DX10CreateTextureFromResource**](d3dx10createtexturefromresource.md)                       | Crie um recurso de textura de outro recurso.                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Interfaces D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
