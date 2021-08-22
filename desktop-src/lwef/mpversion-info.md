---
title: Estrutura de MPVERSION_INFO (MpClient. h)
description: Informações de versão dos componentes do Malware Protection Manager.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- recursos de ambiente de Windows herdado da estrutura de MPVERSION_INFO
- Windows recursos de ambiente herdados do ponteiro de estrutura do PMPVERSION_INFO
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50a89b03b8b310416f9b0b496c055f732f4e83859bb7eba50b7891abebc27d26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608696"
---
# <a name="mpversion_info-structure"></a>Estrutura de informações do MPVERSION \_

Informações de versão dos componentes do Malware Protection Manager.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**Product**
</dt> <dd>

Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versão do produto.

</dd> <dt>

**Serviço**
</dt> <dd>

Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versão do componente de serviço.

</dd> <dt>

**FileSystemFilter**
</dt> <dd>

Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versão do componente de filtro do sistema de arquivos.

</dd> <dt>

**Mecanismo**
</dt> <dd>

Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versão do componente do mecanismo.

</dd> <dt>

**Assignature**
</dt> <dd>

Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versão do componente de assinatura de AntiSpyware.

</dd> <dt>

**AVSignature**
</dt> <dd>

Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versão do componente de assinatura antivírus.

</dd> <dt>

**NISEngine**
</dt> <dd>

Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versão do mecanismo NIS.

</dd> <dt>

**NISSignature**
</dt> <dd>

Tipo: **[ **\_ versão de MPCOMPONENT**](mpcomponent-version.md)**

</dd> <dd>

Versão do componente de assinatura de assinatura NIS.

</dd> <dt>

**Reserved**
</dt> <dd>

Tipo: **[**MPCOMPONENT \_ versão**](mpcomponent-version.md) \[ 4\]**

</dd> <dd>

Campos reservados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>MpClient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**versão do MPCOMPONENT \_**](mpcomponent-version.md)
</dt> </dl>

 

 





