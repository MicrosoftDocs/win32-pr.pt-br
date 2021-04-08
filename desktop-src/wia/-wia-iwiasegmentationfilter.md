---
description: A interface IWiaSegmentationFilter detecta as subregiãos de um fluxo de imagem e torna itens IWiaItem2 separados para cada um.
ms.assetid: eb7f1284-ab98-4d86-8b30-7abd504cee12
title: Interface IWiaSegmentationFilter (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaSegmentationFilter
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: b9c0bcdee5b40c37fb38b390f5085fe275f0f660
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827167"
---
# <a name="iwiasegmentationfilter-interface"></a>Interface IWiaSegmentationFilter

A interface **IWiaSegmentationFilter** detecta as subregiãos de um fluxo de imagem e torna itens [**IWiaItem2**](-wia-iwiaitem2.md) separados para cada um.

## <a name="members"></a>Membros

A interface **IWiaSegmentationFilter** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaSegmentationFilter** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IWiaSegmentationFilter** tem esses métodos.



| Método                                                             | Descrição                                                                                                                                              |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DetectRegions**](-wia-iwiasegmentationfilter-detectregions.md) | Determina as subregiãos de uma imagem disposta no cilindro de mesa para que cada sub-região possa ser adquirida em um item de imagem separado. <br/> |



 

## <a name="remarks"></a>Comentários

Um aplicativo deve usar [**IWiaItem2:: GetExtension**](-wia-iwiaitem2-getextension.md) para criar uma nova instância do filtro de segmentação. Um aplicativo normalmente chama essa função antes de exibir sua janela de visualização.

Ao implementar esse filtro, use [**IWiaItem2:: createchilditem**](-wia-iwiaitem2-createchilditem.md) para criar os itens filho. O aplicativo deve passar **\_ valores de \_ propriedade \_ pai de cópia** para o parâmetro *ICreationFlags* para garantir que as propriedades, como formato de imagem e resolução, sejam as mesmas no filho recém-criado como no item pai.

Um filtro de segmentação deve dar suporte a todos os formatos de imagem para os quais o driver que ele é usado oferece suporte. O filtro fornecido pela Microsoft dá suporte a bitmap (BMP), Graphics Interchange Format (GIF), JPEG, Portable Network Graphics (PNG) e TIFF (Tagged Image File Format).

O filtro de segmentação deve ser usado somente em itens de scanner de filme e de mesa. Para a verificação de filmes, um scanner geralmente vem com os quadros fixos, caso em que o driver criou os itens filho e o aplicativo não deve invocar o filtro de segmentação.

A interface **IWiaSegmentationFilter** , como todas as interfaces de Component Object Model (com), herda os métodos de interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Métodos IUnknown                                        | Descrição                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retorna ponteiros para interfaces com suporte. |
| [IUnknown:: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrementa a contagem de referência.               |
| [IUnknown:: versão](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Decrementa a contagem de referência.               |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
