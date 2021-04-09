---
description: 'O método IWiaItem2:: EnumRegisterEventInfo cria um enumerador que você pode usar para obter informações sobre eventos para os quais um aplicativo está registrado.'
ms.assetid: 9c25e9ae-bd3e-46a6-b4c2-c0bbcd265d51
title: 'Método IWiaItem2:: EnumRegisterEventInfo (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumRegisterEventInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 9b5899b629267f74724129aeae3f66801953d8cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090510"
---
# <a name="iwiaitem2enumregistereventinfo-method"></a>Método IWiaItem2:: EnumRegisterEventInfo

O método **IWiaItem2:: EnumRegisterEventInfo** cria um enumerador que você pode usar para obter informações sobre eventos para os quais um aplicativo está registrado.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumRegisterEventInfo(
  [in]        LONG              lFlags,
  [in]  const GUID              *pEventGUID,
  [out]       IEnumWIA_DEV_CAPS **ppIEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Não usado. Defina como 0.

</dd> <dt>

*pEventGUID* \[ no\]
</dt> <dd>

Tipo: **const GUID \** _

Ponteiro para um identificador que especifica o evento de hardware para o qual você deseja obter informações de registro.

</dd> <dt>

_ppIEnum * \[ out\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

O endereço de um ponteiro para a interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Um aplicativo chama esse método para criar um objeto enumerador para as informações do evento. **IWiaItem2:: EnumRegisterEventInfo** armazena o endereço da interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) do objeto enumerador no parâmetro *ppIEnum* . Em seguida, o programa usa o ponteiro de interface para enumerar as propriedades do evento para o qual ele está registrado.

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIEnum* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl> |



 

 
