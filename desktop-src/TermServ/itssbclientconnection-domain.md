---
title: Propriedade de domínio ITsSbClientConnection
description: Recupera um valor que indica o nome de domínio do cliente de Conexão de Área de Trabalho Remota (RDC).
ms.assetid: 628f450d-10f4-4405-8d7c-ae58c72c2755
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de domínio
- Serviços de Área de Trabalho Remota de propriedade de domínio, interface ITsSbClientConnection
- Serviços de Área de Trabalho Remota de interface ITsSbClientConnection, propriedade de domínio
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Domain
- ITsSbClientConnection.get_Domain
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 678d6fc6838b615faeec9fa36b736b3105b64453
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810978"
---
# <a name="itssbclientconnectiondomain-property"></a>ITsSbClientConnection: Propriedade omain de:D

Recupera um valor que indica o nome de domínio do cliente de Conexão de Área de Trabalho Remota (RDC).

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Domain(
  [out, retval] BSTR *pVal
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para uma variável **BSTR** que contém o nome de domínio do cliente RDC. Quando você terminar de usar a cadeia de caracteres, libere-a chamando a função [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                       |
| INSERI<br/>                      | <dl> <dt>Sbtsv. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbClientConnection**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> </dl>

 

