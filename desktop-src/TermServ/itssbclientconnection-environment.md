---
title: Propriedade de ambiente ITsSbClientConnection
description: Recupera um objeto que contém informações sobre o ambiente que hospeda o computador de destino.
ms.assetid: 97fe4851-96a9-4b23-8ad7-f42b87c655d0
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de propriedade de ambiente
- Propriedade de ambiente Serviços de Área de Trabalho Remota, interface ITsSbClientConnection
- Serviços de Área de Trabalho Remota de interface ITsSbClientConnection, propriedade de ambiente
topic_type:
- apiref
api_name:
- ITsSbClientConnection.Environment
- ITsSbClientConnection.get_Environment
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33cc1c3c8a13a21135ee834950e8c0a60d2794cd4b1edb618e5e67c0744fe3e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072206"
---
# <a name="itssbclientconnectionenvironment-property"></a>Propriedade ITsSbClientConnection:: Environment

Recupera um objeto que contém informações sobre o ambiente que hospeda o computador de destino. Por exemplo, em um cenário de área de trabalho virtual, esse objeto contém informações sobre o computador que hospeda a máquina virtual.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Environment(
  [out, retval] ITsSbEnvironment **ppEnvironment
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para um ponteiro para um objeto de ambiente [**ITsSbEnvironment**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment) .

## <a name="error-codes"></a>Códigos do Erro

Se o método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um valor **HRESULT** que indica o erro. Os valores possíveis incluem, mas não estão limitados a, aqueles na lista a seguir.

<dl> <dt>

\_ponteiro E
</dt> <dd>

O ambiente não foi encontrado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um plug-in de orquestração pode chamar esse método para recuperar informações de ambiente sobre uma máquina virtual de destino.

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

 

 





