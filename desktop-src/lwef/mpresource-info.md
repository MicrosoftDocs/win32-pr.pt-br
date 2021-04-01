---
title: Estrutura de MPRESOURCE_INFO (MpClient. h)
description: Estrutura de informações do recurso.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- Recursos do ambiente Windows herdado da estrutura de MPRESOURCE_INFO
- Ponteiro de estrutura de PMPRESOURCE_INFO recursos de ambiente herdados do Windows
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
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918717"
---
# <a name="mpresource_info-structure"></a>Estrutura de informações do MPRESOURCE \_

Estrutura de informações do recurso.

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

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Identificador do esquema de recursos, como "arquivo" ou "dir".

</dd> <dt>

**Caminho**
</dt> <dd>

Tipo: **PG \_ MIDL \_ String LPWSTR**

</dd> <dd>

Caminho absoluto do recurso, com base no **esquema**.

</dd> <dt>

**Classe**
</dt> <dd>

Tipo: **\_ classe MPRESOURCE**

</dd> <dd>

Esse campo é definido quando o recurso é identificado como parte da ameaça. Ele especifica a classe de recurso, principalmente concreta versus Lated. Pode ser uma combinação desses valores possíveis:



| Valor                                                                                                                                                                                                                                                                        | Significado                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <dt>**MP \_ 0x0000 de classe de recurso \_ \_ desconhecido**</dt> <dt></dt> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <dt>**MP \_ Classe de recurso \_ \_ concreta**</dt> <dt>0x0001</dt> </dl>           | Mutuamente exclusivo com **classe de \_ recurso \_ MP \_ latence**.<br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <dt>**MP \_ Classe de recurso \_ \_ Lated**</dt> <dt>0x0002</dt> </dl>                 | Mutuamente exclusivo com **classe de \_ recurso de MP \_ \_ concreta**.<br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <dt>**MP \_ \_Arquivo de \_ exemplo \_ de classe de recurso**</dt> <dt>0x0004</dt> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <dt>**MP \_ 0x0100 \_ \_ compartilhado de classe de recurso**</dt> <dt></dt> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



 

 





