---
description: Obtém o componente de versão prévia do WIA (Windows Image Acquisition) 2,0.
ms.assetid: 0b773c4c-f080-41fa-8902-4243a80fc67c
title: 'Método IWiaItem2:: GetPreviewComponent (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.GetPreviewComponent
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2e0881f68044c30731322c89d6cc2f19ce7277a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090507"
---
# <a name="iwiaitem2getpreviewcomponent-method"></a>Método IWiaItem2:: GetPreviewComponent

Obtém o componente de versão prévia do WIA (Windows Image Acquisition) 2,0.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetPreviewComponent(
  [in]  LONG        lFlags,
  [out] IWiaPreview **ppWiaPreview
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Não usado. Defina como 0.

</dd> <dt>

*ppWiaPreview* \[ fora\]
</dt> <dd>

Tipo: **[ **IWiaPreview**](-wia-iwiapreview.md)\*\***

Retorna o endereço de um ponteiro para a interface [**IWiaPreview**](-wia-iwiapreview.md) do componente de visualização.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Use essa função para retornar um ponteiro para o endereço do componente de visualização do WIA 2,0 para qualquer objeto [**IWiaItem2**](-wia-iwiaitem2.md) na árvore de objetos de um dispositivo de hardware WIA 2,0.

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppWiaPreview* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IWiaPreview**](-wia-iwiapreview.md)
</dt> </dl>

 

 
