---
description: Cria uma árvore hierárquica de objetos IWiaItem2 para um dispositivo de aquisição de imagem do Windows (WIA) 2,0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'Método IWiaDevMgr2:: CreateDevice (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a548a0ef43c2621b77c4ed10acde393af21d596d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828456"
---
# <a name="iwiadevmgr2createdevice-method"></a>Método IWiaDevMgr2:: CreateDevice

Cria uma árvore hierárquica de objetos [**IWiaItem2**](-wia-iwiaitem2.md) para um dispositivo de aquisição de imagem do Windows (WIA) 2,0.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Atualmente não utilizado. Deve ser definido como zero.

</dd> <dt>

*bstrDeviceID* \[ no\]
</dt> <dd>

Tipo: **BSTR**

Especifica o identificador exclusivo do dispositivo WIA 2,0.

</dd> <dt>

*ppWiaItem2Root* \[ fora\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recebe o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item raiz na árvore hierárquica do dispositivo WIA 2,0.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Os aplicativos usam o método **IWiaDevMgr2:: CreateDevice** para criar um objeto de dispositivo para os dispositivos WIA 2,0 especificados pelo parâmetro bstrDeviceID. Quando ele retorna, o método **IWiaDevMgr2:: CreateDevice** armazena um endereço de um ponteiro no parâmetro *ppWiaItem2Root*, que aponta para o item raiz da árvore de objetos [**IWiaItem2**](-wia-iwiaitem2.md) criados por **IWiaDevMgr2:: CreateDevice**. Os aplicativos podem usar essa árvore de objetos para controlar e recuperar dados do dispositivo WIA 2,0.

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros recebidos por meio do parâmetro *ppWiaItem2Root* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
