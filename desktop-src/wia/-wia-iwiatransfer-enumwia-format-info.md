---
description: Cria um enumerador para os formatos de transferência aos quais o dispositivo de aquisição de imagem do Windows (WIA) 2,0 dá suporte.
ms.assetid: 70fffc7b-b500-4404-9d94-76d1828ddc8c
title: 'Método IWiaTransfer:: EnumWIA_FORMAT_INFO (WIA. h)'
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
ms.openlocfilehash: 66f3c91d6023655daf85b2a0d726d98a685b001b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770475"
---
# <a name="iwiatransferenumwia_format_info-method"></a>Método de informações de \_ formato IWiaTransfer:: EnumWIA \_

Cria um enumerador para os formatos de transferência aos quais o dispositivo de aquisição de imagem do Windows (WIA) 2,0 dá suporte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumWIA_FORMAT_INFO(
  [out] IEnumWIA_FORMAT_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppIEnum* \[ fora\]
</dt> <dd>

Tipo: **[ **\_ \_ informações de formato IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info)\*\***

O endereço do ponteiro para a interface [**de \_ \_ informações de formato IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_format_info) para o enumerador.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) no ponteiro de interface recebido por meio do parâmetro *ppIEnum* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                   |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
