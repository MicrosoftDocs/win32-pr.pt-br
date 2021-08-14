---
description: cria um enumerador de informações de propriedade para cada dispositivo disponível 2,0 WIA (aquisição de imagem Windows).
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'Método IWiaDevMgr2:: EnumDeviceInfo (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 8b646c494d9793986373d45db2d89dfde91e744196d86d28aceab35874f504d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208718"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a>Método IWiaDevMgr2:: EnumDeviceInfo

cria um enumerador de informações de propriedade para cada dispositivo disponível 2,0 WIA (aquisição de imagem Windows).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ no\]
</dt> <dd>

Tipo: **longo**

Especifica o tipo de dispositivos WIA 2,0 a serem enumerados.

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**\_local de \_ enumeração \_ DevInfo do WIA**


</dt> <dd>

Somente dispositivos de scanner ativos conectados localmente são enumerados.

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**\_Enumeração DevInfo do WIA \_ \_ All**


</dt> <dd>

Todos os dispositivos são enumerados, localmente e remoto, incluindo dispositivos inativos (desconectados) e dispositivos STI herdados.

</dd> </dl> </dd> <dt>

*ppIEnum* \[ out, retval\]
</dt> <dd>

Tipo: **[ **\_ \_ informações de desenvolvimento de IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***

Recebe o endereço de um ponteiro para a interface de [**\_ \_ informações de dev IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="remarks"></a>Comentários

O método **IWiaDevMgr2:: EnumDeviceInfo** cria um objeto enumerador que dá suporte à interface [**\_ \_ informações de desenvolvimento IEnumWIA**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . O método armazena um ponteiro para a interface de **\_ \_ informações de dev IEnumWIA** no parâmetro *ppIEnum*. Os aplicativos podem usar o ponteiro de interface de **\_ \_ informações de desenvolvimento IEnumWIA** para enumerar as propriedades de cada dispositivo WIA 2,0 conectado ao computador do usuário.

Os aplicativos devem chamar o método [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface recebidos por meio do parâmetro *ppIEnum* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                               |
| parâmetro<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
