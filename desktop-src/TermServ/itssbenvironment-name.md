---
title: Propriedade ITsSbEnvironment Name
description: Recupera um valor que indica o nome do ambiente que hospeda o computador de destino.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Nome da propriedade Serviços de Área de Trabalho Remota
- Propriedade name Serviços de Área de Trabalho Remota interface , ITsSbEnvironment
- Interface ITsSbEnvironment Serviços de Área de Trabalho Remota , propriedade Name
topic_type:
- apiref
api_name:
- ITsSbEnvironment.Name
- ITsSbEnvironment.get_Name
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d60f64cf8bc350ca80072b2c7a43ecabf2fbe5d4650188b7d5a5e5c05a4fbc7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072196"
---
# <a name="itssbenvironmentname-property"></a>Propriedade ITsSbEnvironment::Name

Recupera um valor que indica o nome do ambiente que hospeda o computador de destino.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para uma **variável BSTR** que contém o nome do ambiente.

## <a name="remarks"></a>Comentários

Esse método retorna uma cadeia de caracteres que não é usada diretamente pelo Conexão de Área de Trabalho Remota Broker (Agente de Conexão de RD). O Agente de Conexão RD passa essa cadeia de caracteres para plug-ins de recursos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| Idl<br/>                      | <dl> <dt>Sbtsv.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





