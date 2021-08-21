---
description: Método SetSecurityPolicy da classe Msvm_SecurityService - Define o protetor de chave para um sistema virtual.
ms.assetid: 22496fde-6298-4e9d-bd0c-135dcb4ea5a5
title: Método SetSecurityPolicy da Msvm_SecurityService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService.SetSecurityPolicy
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c3ce4e95fe99eca0616d886ca16fefcb771be50f1a8cc0a46e6780e0411a6ad1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147090"
---
# <a name="setsecuritypolicy-method-of-the-msvm_securityservice-class"></a>Método SetSecurityPolicy da classe Msvm \_ SecurityService

Define o protetor de chave para um sistema virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetSecurityPolicy(
  [in]  string              SecuritySettingData,
  [in]  uint8               SecurityPolicy[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SecuritySettingData* \[ Em\]
</dt> <dd>

A cadeia de caracteres contém uma instância inserida da [**classe Msvm \_ SecuritySettingData**](msvm-securitysettingdata.md) que representa as configurações de segurança de um sistema virtual.

</dd> <dt>

*SecurityPolicy* \[ Em\]
</dt> <dd>

Matriz de byte bruto que contém a política de segurança a ser definida.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Um parâmetro opcional para monitorar o progresso da operação, que será usado se o método não puder ser executado de forma síncrona. Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

On, success, retorna um 0; caso contrário, retornará um erro.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Parâmetros de método verificados – Trabalho iniciado** (4096)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

**O status é desconhecido** (32771)
</dt> <dt>

**Tempoout** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

**O sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

**O sistema não está disponível** (32777)
</dt> <dt>

**Memória sem memória** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1703 somente \[ aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ SecurityService**](msvm-securityservice.md)
</dt> </dl>

 

 




