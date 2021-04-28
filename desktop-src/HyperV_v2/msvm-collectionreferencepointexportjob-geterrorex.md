---
description: Método GetErrorEx da classe Msvm_CollectionReferencePointExportJob – recupera informações adicionais sobre um erro.
ms.assetid: 64a90f18-3ae7-4021-857f-64adf8c40430
title: Método GetErrorEx da classe Msvm_CollectionReferencePointExportJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3b84c41776c081c302078773d9402145b0fe41e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112084"
---
# <a name="geterrorex-method-of-the-msvm_collectionreferencepointexportjob-class"></a>Método GetErrorEx da \_ classe CollectionReferencePointExportJob Msvm

Recupera informações adicionais sobre um erro. Quando o trabalho está em execução ou foi encerrado sem erro, **GetErrorEx** não retorna nenhuma instância de [**\_ erro Msvm**](msvm-error.md) . No entanto, se o trabalho falhou devido a algum problema interno ou porque o trabalho foi encerrado por um cliente, **GetErrorEx** retorna uma ou mais instâncias de **\_ erro Msvm** .

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Erros* \[ do fora\]
</dt> <dd>

Se o status operacional do trabalho não for "OK", esse parâmetro retornará uma matriz de instâncias [**de \_ erro Msvm**](msvm-error.md) . Caso contrário, se o trabalho for "OK", esse parâmetro conterá **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Em caso de sucesso, retorna 0; caso contrário, retorna um dos seguintes valores de erro:

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

O **status é desconhecido** (32771)
</dt> <dt>

**Tempo limite** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

O **sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

O **sistema não está disponível** (32777)
</dt> <dt>

**Memória insuficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Msvm \_ CollectionReferencePointExportJob**](msvm-collectionreferencepointexportjob.md)
</dt> </dl>

 

 




