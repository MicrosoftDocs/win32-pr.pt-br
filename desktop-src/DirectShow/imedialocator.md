---
description: A interface IMediaLocator fornece métodos para validar nomes de arquivo nos serviços de edição do DirectShow (DES).
ms.assetid: 6c1ae957-a2be-454b-9451-772e4a670677
title: Interface IMediaLocator (QEdit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaLocator
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9664bf793e989c5975bcef0e712a550399c4ddee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759074"
---
# <a name="imedialocator-interface"></a>Interface IMediaLocator

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IMediaLocator` interface fornece métodos para validar nomes de arquivo nos [serviços de edição do DirectShow](directshow-editing-services.md) (des). Use essa interface para garantir que um determinado nome de arquivo e caminho correspondam a um arquivo existente. Essa interface também fornece uma maneira de Pesquisar o arquivo em outros locais e exibir uma caixa de diálogo **aberta** para que o usuário possa localizar o arquivo.

O localizador de mídia implementa essa interface. A linha do tempo e o mecanismo de processamento também dão suporte à validação de nome de arquivo por meio dos seguintes métodos:

-   [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md): valida e atualiza os nomes de arquivo na linha do tempo.
-   [**IRenderEngine:: SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md): especifica como o mecanismo de renderização valida nomes de arquivo no momento da renderização.

Normalmente, um aplicativo DES chamará esses métodos em vez de criar diretamente uma instância do localizador de mídia. Para obter mais informações, consulte [usando o localizador de mídia](using-the-media-locator.md).

## <a name="members"></a>Membros

A interface **IMediaLocator** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMediaLocator** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IMediaLocator** tem esses métodos.



| Método                                                     | Descrição                                                                        |
|:-----------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**AddFoundLocation**](imedialocator-addfoundlocation.md) | Adiciona um diretório ao cache de diretório.<br/>                                |
| [**FindMediaFile**](imedialocator-findmediafile.md)       | Procura um arquivo e, se for bem-sucedido, recupera o caminho para o arquivo.<br/> |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
