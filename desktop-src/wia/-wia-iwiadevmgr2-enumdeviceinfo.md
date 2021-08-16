---
description: Cria um enumerador de informações de propriedade para cada dispositivo WIA (Aquisição de Imagem) 2.0 Windows disponível.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: Método IWiaDevMgr2::EnumDeviceInfo (Wia.h)
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
# <a name="iwiadevmgr2enumdeviceinfo-method"></a>Método IWiaDevMgr2::EnumDeviceInfo

Cria um enumerador de informações de propriedade para cada dispositivo WIA (Aquisição de Imagem) 2.0 Windows disponível.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lFlags* \[ Em\]
</dt> <dd>

Tipo: **LONG**

Especifica o tipo de dispositivos WIA 2.0 a ser enumerado.

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA \_ DEVINFO \_ ENUM \_ LOCAL**


</dt> <dd>

Somente dispositivos de scanner ativos conectados localmente são enumerados.

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA \_ DEVINFO \_ ENUM \_ ALL**


</dt> <dd>

Todos os dispositivos são enumerados, localmente e remotos, incluindo dispositivos inativos (desconectados) e dispositivos herdados somente DEEI.

</dd> </dl> </dd> <dt>

*ppIEnum* \[ out, retval\]
</dt> <dd>

Tipo: **[ **IEnumWIA \_ DEV \_ INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***

Recebe o endereço de um ponteiro para a interface [**IEnumWIA \_ DEV \_ INFO.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **HRESULT**

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="remarks"></a>Comentários

O **método IWiaDevMgr2::EnumDeviceInfo** cria um objeto enumerador que dá suporte à interface [**IEnumWIA \_ DEV \_ INFO.**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) O método armazena um ponteiro para a interface **IEnumWIA \_ DEV \_ INFO** no parâmetro *ppIEnum*. Os aplicativos podem usar o ponteiro de interface **IEnumWIA \_ DEV \_ INFO** para enumerar as propriedades de cada dispositivo WIA 2.0 anexado ao computador do usuário.

Os aplicativos devem chamar [o método IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) nos ponteiros de interface que recebem por meio do *parâmetro ppIEnum.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                     |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                               |
| Cabeçalho<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 
