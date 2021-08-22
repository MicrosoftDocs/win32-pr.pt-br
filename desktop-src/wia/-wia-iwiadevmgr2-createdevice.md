---
description: Cria uma árvore hierárquica de objetos IWiaItem2 para um dispositivo WIA (Aquisição Windows Imagem) 2.0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: Método IWiaDevMgr2::CreateDevice (Wia.h)
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
ms.openlocfilehash: a40267e77671b807f0e6969845a3a5a7096694e4f4e7978467ee9ca5909284d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965725"
---
# <a name="iwiadevmgr2createdevice-method"></a>Método IWiaDevMgr2::CreateDevice

Cria uma árvore hierárquica [**de objetos IWiaItem2**](-wia-iwiaitem2.md) para um dispositivo WIA (Aquisição de Imagem) 2.0 do Windows.

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

*lFlags* \[ Em\]
</dt> <dd>

Tipo: **LONG**

Atualmente não éusado. Deve ser definido como zero.

</dd> <dt>

*bstrDeviceID* \[ Em\]
</dt> <dd>

Tipo: **BSTR**

Especifica o identificador exclusivo do dispositivo WIA 2.0.

</dd> <dt>

*ppWiaItem2Root* \[ out\]
</dt> <dd>

Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

Recebe o endereço de um ponteiro para a interface [**IWiaItem2**](-wia-iwiaitem2.md) do item raiz na árvore hierárquica para o dispositivo WIA 2.0.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

Os aplicativos usam o método **IWiaDevMgr2::CreateDevice** para criar um objeto de dispositivo para os dispositivos WIA 2.0 especificados pelo parâmetro bstrDeviceID. Quando retorna, o método **IWiaDevMgr2::CreateDevice** armazena um endereço de um ponteiro no parâmetro *ppWiaItem2Root*, que aponta para o item raiz da árvore de objetos [**IWiaItem2**](-wia-iwiaitem2.md) criados por **IWiaDevMgr2::CreateDevice**. Os aplicativos podem usar essa árvore de objetos para controlar e recuperar dados do dispositivo WIA 2.0.

Os aplicativos devem chamar o método [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros recebidos por meio do *parâmetro ppWiaItem2Root.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
