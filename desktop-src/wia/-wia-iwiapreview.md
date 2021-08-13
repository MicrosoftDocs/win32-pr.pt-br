---
description: A interface IWiaPreview armazena em cache imagens não filtradas internamente e as passa por filtros de processamento de imagem.
ms.assetid: 8a51c42b-aa1d-4df0-aba3-6aeb8e1ca2cf
title: Interface IWiaPreview (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: e2672211e5c1a17fa360a6078069ae8260687dc896843ffb6bf572d9b7be8caa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442066"
---
# <a name="iwiapreview-interface"></a>Interface IWiaPreview

A interface **IWiaPreview** armazena em cache imagens não filtradas internamente e as passa por filtros de processamento de imagem.

## <a name="members"></a>Membros

A interface **IWiaPreview** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **O IWiaPreview** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWiaPreview** tem esses métodos.



| Método                                                  | Descrição                                                                                                                                                                                 |
|:--------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Limpar**](-wia-iwiapreview-clear.md)                 | Libera a imagem não filtrada armazenada em cache pelo [**método IWiaPreview::GetNewPreview.**](-wia-iwiapreview-getnewpreview.md) Ele também libera o filtro de processamento de imagem. <br/>          |
| [**DetectRegions**](-wia-iwiapreview-detectregions.md) | Invoca o filtro de segmentação de driver e passa a imagem não filtrada armazenada em cache pelo método [**IWiaPreview::GetNewPreview**](-wia-iwiapreview-getnewpreview.md) para o filtro. <br/> |
| [**GetNewPreview**](-wia-iwiapreview-getnewpreview.md) | Armazena em cache internamente a imagem não filtrada retornada do driver. <br/>                                                                                                                |
| [**UpdatePreview**](-wia-iwiapreview-updatepreview.md) | Obtém a imagem não filtrada armazenada em cache pelo [**método IWiaPreview::GetNewPreview.**](-wia-iwiapreview-getnewpreview.md) <br/>                                                            |



 

## <a name="remarks"></a>Comentários

Esse filtro é chamado automaticamente pelo [**método IWiaTransfer::D ownload.**](-wia-iwiatransfer-download.md)

A interface **IWiaPreview,** como todas Component Object Model INTERFACES (COM), herda os métodos de interface [IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)



| Métodos IUnknown                                        | Descrição                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retorna ponteiros para interfaces com suporte. |
| [IUnknown::AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa a contagem de referência.               |
| [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Contagem de referências de decrementos.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
