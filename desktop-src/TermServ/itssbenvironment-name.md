---
title: Propriedade de nome ITsSbEnvironment
description: Recupera um valor que indica o nome do ambiente que hospeda o computador de destino.
ms.assetid: 8104bdae-f445-425b-b326-cc3333839d29
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de nome
- Propriedade Name Serviços de Área de Trabalho Remota, interface ITsSbEnvironment
- Serviços de Área de Trabalho Remota de interface ITsSbEnvironment, Propriedade Name
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
ms.openlocfilehash: 2b5ac2fd725ec07102c08e93b2bfb39dabe701ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918191"
---
# <a name="itssbenvironmentname-property"></a>Propriedade ITsSbEnvironment:: Name

Recupera um valor que indica o nome do ambiente que hospeda o computador de destino.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Name(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para uma variável **BSTR** que contém o nome do ambiente.

## <a name="remarks"></a>Comentários

Esse método retorna uma cadeia de caracteres que não é usada diretamente pelo agente de Conexão de Área de Trabalho Remota (agente de conexão RD). O agente de conexão RD passa essa cadeia de caracteres para plug-ins de recurso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| INSERI<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> </dl>

 

 





