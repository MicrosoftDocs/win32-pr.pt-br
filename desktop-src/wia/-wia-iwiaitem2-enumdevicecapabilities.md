---
description: Cria um enumerador que é usado para verificar os comandos e eventos aos quais um dispositivo de aquisição de imagem do Windows (WIA) 2,0 dá suporte.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'Método IWiaItem2:: EnumDeviceCapabilities (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3e771aa636b42d9cd7e4024a1684ebe3edf02eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501794"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a>Método IWiaItem2:: EnumDeviceCapabilities

Cria um enumerador que é usado para verificar os comandos e eventos aos quais um dispositivo de aquisição de imagem do Windows (WIA) 2,0 dá suporte.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Especifica um sinalizador que seleciona o tipo de recursos a serem enumerados. É um dos valores a seguir.

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**\_comandos do dispositivo WIA \_**


</dt> <dd>

Enumere os comandos do dispositivo.

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**\_eventos do dispositivo WIA \_**


</dt> <dd>

Enumerar eventos de dispositivo.

</dd> </dl> </dd> <dt>

*ppIEnumWIA \_ \_* Desativação de desenvolvimento \[\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***

Recebe um ponteiro para a interface [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) criada por esse método.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

Esse método é usado para criar um objeto de enumerador para obter o conjunto de comandos e eventos aos quais um dispositivo WIA 2,0 dá suporte. O parâmetro *lFlags* é usado para especificar quais tipos de recursos de dispositivo serão enumerados. O método **IWiaItem2:: EnumDeviceCapabilities** armazena o endereço da interface do objeto enumerador no parâmetro *ppIEnumWIA \_ dev \_ Caps* .

Esse método só pode ser chamado no item raiz dos objetos [**IWiaItem2**](-wia-iwiaitem2.md) de uma árvore de dispositivos.

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIEnumWIA \_ dev \_ Caps* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
