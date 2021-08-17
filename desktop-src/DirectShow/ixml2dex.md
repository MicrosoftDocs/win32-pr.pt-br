---
description: A interface IXml2Dex salva e carrega DirectShow de projeto do DES (Serviços de Edição) linguagem XML (XML). Essa interface também fornece métodos para ler e escrever arquivos DirectShow grafo (.grf).
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: Interface IXml2Dex (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3bc12c2305a8b92110d4aa17522184e9a3c5ee83b60ccd5a989468fa0a8c6e7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952385"
---
# <a name="ixml2dex-interface"></a>Interface IXml2Dex

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IXml2Dex` interface salva e carrega DirectShow [de](directshow-editing-services.md) projeto do DES (Serviços de Edição) linguagem XML (XML). Essa interface também fornece métodos para ler e escrever arquivos DirectShow grafo (.grf).

## <a name="members"></a>Membros

A interface **IXml2Dex** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IXml2Dex** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IXml2Dex** tem esses métodos.



| Método                                                      | Descrição                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**CopyXML**](ixml2dex-copyxml.md)                         | Não implementado.<br/>                                                |
| [**CreateGraphFromFile**](ixml2dex-creategraphfromfile.md) | Não implementado.<br/>                                                |
| [**Excluir**](ixml2dex-delete.md)                           | Não implementado.<br/>                                                |
| [**PasteXML**](ixml2dex-pastexml.md)                       | Não implementado.<br/>                                                |
| [**PasteXMLFile**](ixml2dex-pastexmlfile.md)               | Não implementado.<br/>                                                |
| [**Readxml**](ixml2dex-readxml.md)                         | Não implementado.<br/>                                                |
| [**ReadXMLFile**](ixml2dex-readxmlfile.md)                 | Carrega um arquivo de projeto XML.<br/>                                      |
| [**Redefinir**](ixml2dex-reset.md)                             | Não implementado.<br/>                                                |
| [**WriteGrfFile**](ixml2dex-writegrffile.md)               | Grava um grafo de filtro em um arquivo no formato .grf.<br/>                 |
| [**Writexml**](ixml2dex-writexml.md)                       | Converte uma linha do tempo em uma cadeia de caracteres XML.<br/>                         |
| [**WriteXMLFile**](ixml2dex-writexmlfile.md)               | Converte uma linha do tempo em XML e grava os dados XML em um arquivo.<br/> |
| [**WriteXMLPart**](ixml2dex-writexmlpart.md)               | Não implementado.<br/>                                                |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de título Qedit.h não é compatível com os headers direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o Qedit.h, baixe [o Microsoft Windows SDK Update para Windows Vista e .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O Qedit.h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Internet Explorer 4.0 ou posterior<br/>                                               |
| Cabeçalho<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
