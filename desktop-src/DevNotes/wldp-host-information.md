---
description: Uma estrutura que identifica o host e o arquivo de origem a serem avaliados.
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: Estrutura de WLDP_HOST_INFORMATION (Wldp. h)
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
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010101"
---
# <a name="wldp_host_information-structure"></a>Estrutura de informações do \_ host WLDP \_

Uma estrutura que identifica o host e o arquivo de origem a serem avaliados.

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

Deve ser **a \_ \_ \_ revisão de informações do host WLDP**.

</dd> <dt>

**dwHostId**
</dt> <dd>

Valor de enumeração [**da \_ \_ ID de host WLDP**](wldp-host-id.md) que descreve a ID do host.

</dd> <dt>

**szSource**
</dt> <dd>

Caminho completo e nome do script com a extensão. NULL para **WLDP \_ de \_ ID \_ de host global** ou execução de script manual.

</dd> <dt>

**hSource**
</dt> <dd>

Além do nome, o chamador pode especificar um identificador para o arquivo usado para validação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Wldp. h</dt> </dl> |



 

 




