---
description: Identifica o tipo de host do chamador WLDP.
ms.assetid: E8E603CC-9CB2-4C3B-9F06-9B06C7B5D752
title: Enumeração de WLDP_HOST_ID (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_ID
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: fa52bc6259c75d5bb0929cb25610beb2b143515e2874b09bf04c454397a909e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758376"
---
# <a name="wldp_host_id-enumeration"></a>Enumeração de ID de \_ host WLDP \_

Identifica o tipo de host do chamador WLDP.

## <a name="syntax"></a>Syntax


```C++
typedef enum _WLDP_HOST_ID { 
   WLDP_HOST_ID_UNKNOWN     = 0,
   WLDP_HOST_ID_GLOBAL      = 1,
  WLDP_HOST_ID_VBA          = 2,
   WLDP_HOST_ID_WSH         = 3,
   WLDP_HOST_ID_POWERSHELL  = 4,
   WLDP_HOST_ID_IE          = 5,
   WLDP_HOST_ID_MSI         = 6,
   WLDP_HOST_ID_MAX         = 7
} WLDP_HOST_ID, *PWLDP_HOST_ID;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="_WLDP_HOST_ID_UNKNOWN_"></span><span id="_wldp_host_id_unknown_"></span>**WLDP \_ ID de HOST \_ \_ desconhecida** 
</dt> <dd>

O tipo de host é desconhecido.

</dd> <dt>

<span id="_WLDP_HOST_ID_GLOBAL"></span><span id="_wldp_host_id_global"></span>**WLDP \_ ID do HOST \_ \_ global**
</dt> <dd>

O tipo de host é política global.

</dd> <dt>

<span id="WLDP_HOST_ID_VBA"></span><span id="wldp_host_id_vba"></span>**WLDP \_ ID do host do \_ \_ VBA**
</dt> <dd>

O tipo de host é VBScript.

</dd> <dt>

<span id="_WLDP_HOST_ID_WSH"></span><span id="_wldp_host_id_wsh"></span>**WLDP \_ ID do HOST \_ \_ WSH**
</dt> <dd>

o tipo de host é Windows host de Script.

</dd> <dt>

<span id="_WLDP_HOST_ID_POWERSHELL"></span><span id="_wldp_host_id_powershell"></span>**WLDP \_ ID do HOST \_ \_ PowerShell**
</dt> <dd>

o tipo de host é Windows Powershell.

</dd> <dt>

<span id="_WLDP_HOST_ID_IE"></span><span id="_wldp_host_id_ie"></span>**WLDP \_ ID do HOST \_ \_ IE**
</dt> <dd>

O tipo de host é o Internet Explorer.

</dd> <dt>

<span id="_WLDP_HOST_ID_MSI"></span><span id="_wldp_host_id_msi"></span>**WLDP \_ \_ \_ MSI da ID do host**
</dt> <dd>

o tipo de host é o Microsoft Windows Installer.

</dd> <dt>

<span id="_WLDP_HOST_ID_MAX__"></span><span id="_wldp_host_id_max__"></span>**WLDP \_ ID do HOST \_ \_ máx** . 
</dt> <dd>

O valor máximo de enumeração.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Wldp. h</dt> </dl> |



 

 




