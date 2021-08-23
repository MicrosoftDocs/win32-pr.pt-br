---
title: MPRESOURCE_INFO (MpClient.h)
description: Estrutura de informações de recurso.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- MPRESOURCE_INFO estrutura herdada Windows recursos de ambiente
- PMPRESOURCE_INFO de estrutura herdada Windows recursos de ambiente
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c399beceba4551ba3269e86f5f3c30c6967f31b4dbc5f303225e8cbfc1667df4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747419"
---
# <a name="mpresource_info-structure"></a>Estrutura MPRESOURCE \_ INFO

Estrutura de informações de recurso.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Esquema**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Identificador de esquema de recursos, como "file" ou "dir".

</dd> <dt>

**Caminho**
</dt> <dd>

Tipo: **MP \_ MIDL STRING \_ LPWSTR**

</dd> <dd>

Caminho absoluto do recurso, com base no **Esquema**.

</dd> <dt>

**Classe**
</dt> <dd>

Tipo: **CLASSE MPRESOURCE \_**

</dd> <dd>

Esse campo é definido quando o recurso é identificado como parte da ameaça. Especifica a classe de recurso, principalmente concreta versus latente. Pode ser uma combinação desses valores possíveis:



| Valor                                                                                                                                                                                                                                                                        | Significado                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <dt>**MP \_ RESOURCE \_ CLASS \_ UNKNOWN**</dt> <dt>0x0000</dt> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <dt>**MP \_ CLASSE \_ DE \_ RECURSO CONCRETE**</dt> <dt>0x0001</dt> </dl>           | Mutuamente exclusivo com **MP \_ RESOURCE CLASS \_ \_ LATENT.**<br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <dt>**MP \_ CLASSE \_ DE \_ RECURSO LATENTE**</dt> <dt>0X0002</dt> </dl>                 | Mutuamente exclusivo com **MP \_ RESOURCE CLASS \_ \_ CONCRETE.**<br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <dt>**MP \_ ARQUIVO \_ DE EXEMPLO DA CLASSE \_ \_ DE**</dt> <dt>RECURSO 0x0004</dt> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <dt>**MP \_ CLASSE \_ DE RECURSO COMPARTILHADO \_ 0X0100**</dt> <dt></dt> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient.h</dt> </dl> |



 

 





