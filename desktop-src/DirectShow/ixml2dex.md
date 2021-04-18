---
description: A interface IXml2Dex salva e carrega arquivos de projeto de serviços de edição do DirectShow (DES) em linguagem XML (XML). Essa interface também fornece métodos para ler e gravar arquivos do grafo do DirectShow (. GRF).
ms.assetid: a07b0cbe-1f1d-4ccd-a994-9bb1a49c78d8
title: Interface IXml2Dex (QEdit. h)
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
ms.openlocfilehash: ac15110aa1482c37a835ae874057a792e310fc2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780049"
---
# <a name="ixml2dex-interface"></a>Interface IXml2Dex

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

A `IXml2Dex` interface salva e carrega arquivos de projeto de [serviços de edição do DirectShow](directshow-editing-services.md) (DES) em linguagem XML (XML). Essa interface também fornece métodos para ler e gravar arquivos do grafo do DirectShow (. GRF).

## <a name="members"></a>Membros

A interface **IXml2Dex** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IXml2Dex** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IXml2Dex** tem esses métodos.



| Método                                                      | Descrição                                                                |
|:------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**CopyXML**](ixml2dex-copyxml.md)                         | Não implementado.<br/>                                                |
| [**CreateGraphFromFile**](ixml2dex-creategraphfromfile.md) | Não implementado.<br/>                                                |
| [**Apagar**](ixml2dex-delete.md)                           | Não implementado.<br/>                                                |
| [**PasteXML**](ixml2dex-pastexml.md)                       | Não implementado.<br/>                                                |
| [**PasteXMLFile**](ixml2dex-pastexmlfile.md)               | Não implementado.<br/>                                                |
| [**ReadXML**](ixml2dex-readxml.md)                         | Não implementado.<br/>                                                |
| [**ReadXMLfile**](ixml2dex-readxmlfile.md)                 | Carrega um arquivo de projeto XML.<br/>                                      |
| [**Redefinir**](ixml2dex-reset.md)                             | Não implementado.<br/>                                                |
| [**WriteGrfFile**](ixml2dex-writegrffile.md)               | Grava um gráfico de filtro em um arquivo no formato. GRF.<br/>                 |
| [**WriteXML**](ixml2dex-writexml.md)                       | Traduz uma linha do tempo para uma cadeia de caracteres XML.<br/>                         |
| [**WriteXMLfile**](ixml2dex-writexmlfile.md)               | Traduz uma linha do tempo para XML e grava os dados XML em um arquivo.<br/> |
| [**WriteXMLPart**](ixml2dex-writexmlpart.md)               | Não implementado.<br/>                                                |



 

## <a name="remarks"></a>Comentários

> [!Note]  
> O arquivo de cabeçalho QEdit. h não é compatível com cabeçalhos do Direct3D posteriores à versão 7.

 

> [!Note]  
> Para obter o QEdit. h, baixe a [atualização SDK do Microsoft Windows para Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). O QEdit. h não está disponível no SDK do Microsoft Windows para Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versão<br/> | Internet Explorer 4,0 ou posterior<br/>                                               |
| parâmetro<br/>  | <dl> <dt>QEdit. h</dt> </dl>      |
| Biblioteca<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
