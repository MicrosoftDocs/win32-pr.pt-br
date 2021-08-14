---
description: Cria um enumerador para os formatos de transferência aos Windows WIA (Image Acquisition) 2.0.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: Método IWiaTransfer::EnumWIA_FORMAT_INFO (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer.EnumWIA_FORMAT_INFO
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 5e497d389646249c03bfaa4ac8625ce2a440b97f4ff6b8c0b0942ec957d0901e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117669471"
---
# <a name="iwiatransferenumwia_format_info-method"></a>Método IWiaTransfer::EnumWIA \_ FORMAT \_ INFO

Cria um enumerador para os formatos de transferência aos Windows WIA (Image Acquisition) 2.0.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppIEnum* \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ FORMAT \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***

O endereço do ponteiro para a interface [**IEnumWIA \_ FORMAT \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) para o enumerador.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Os aplicativos devem chamar [o método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) no ponteiro de interface recebido por meio do *parâmetro ppIEnum.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                   |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>       |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid.lib</dt> </dl> |



 

 
