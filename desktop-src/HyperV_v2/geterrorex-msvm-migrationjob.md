---
description: Recupera os objetos de erro para o trabalho de migração, se existirem.
ms.assetid: 8526e28c-bfc8-42b3-850c-0a875a52a42c
title: Método GetErrorEx da classe Msvm_MigrationJob classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a6cb3b1b380708a3be259bfd4f9c6ae07bb7e401506dcfe76f2fcf1299ed5d18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995239"
---
# <a name="geterrorex-method-of-the-msvm_migrationjob-class"></a>Método GetErrorEx da classe Msvm \_ MigrationJob

Recupera os objetos de erro para o trabalho de migração, se existirem. Quando o trabalho está em execução ou foi encerrado sem erro, esse método não retorna nenhuma [**instância de erro Msvm. \_**](msvm-error.md) No entanto, se o trabalho tiver falhado devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, uma ou mais instâncias de Erro de **Msvm \_** serão retornadas.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Erros* \[ out\]
</dt> <dd>

Se o status operacional do trabalho não for 2 (OK), esse método retornará uma ou mais instâncias inseridas da [**classe Msvm \_ Error,**](msvm-error.md) no formato CIM-XML, que representam os erros encontrados no trabalho. Se o status operacional do trabalho for 2 (OK), **Null** será retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
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

**O sistema está em usado** (32774)
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
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ MigrationJob**](msvm-migrationjob.md)
</dt> </dl>

 

 




