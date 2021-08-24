---
description: Uma estrutura que identifica o host e o arquivo de origem a ser avaliado.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: WLDP_HOST_INFORMATION (Wldp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: cc1bed8fd104b4aa6abb83d3eb7e19faa37a0301429312c8f0799e256ce32ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404065"
---
# <a name="wldp_host_information-structure"></a>Estrutura de INFORMAÇÕES DO HOST WLDP \_ \_

Uma estrutura que identifica o host e o arquivo de origem a ser avaliado.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwRevision**
</dt> <dd>

Deve ser **WLDP \_ HOST INFORMATION \_ \_ REVISION**.

</dd> <dt>

**dwHostId**
</dt> <dd>

Valor de enumeração da [**ID do \_ HOST \_ WLDP**](wldp-host-id.md) que descreve a ID do host.

</dd> <dt>

**szSource**
</dt> <dd>

Caminho completo e nome do script com a extensão. NULL para **a \_ \_ ID \_ DE HOST GLOBAL do WLDP** ou execução manual de script.

</dd> <dt>

**hSource**
</dt> <dd>

Além do nome, o chamador pode especificar um handle para o arquivo usado para validação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Wldp.h</dt> </dl> |



 

 




