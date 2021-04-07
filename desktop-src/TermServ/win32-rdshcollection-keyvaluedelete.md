---
title: Método KeyValueDelete da classe Win32_RDSHCollection
description: Exclui a chave especificada (e o valor associado) da coleção.
ms.assetid: 968d6744-7b4a-45e5-87fb-90c408dbc771
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método KeyValueDelete
- Método KeyValueDelete Serviços de Área de Trabalho Remota, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Serviços de Área de Trabalho Remota, método KeyValueDelete
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueDelete
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1b4b29aea7890817c8d3cd8599f6effceb53c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918308"
---
# <a name="keyvaluedelete-method-of-the-win32_rdshcollection-class"></a>Método KeyValueDelete da classe Win32 \_ RDSHCollection

Exclui a chave especificada (e o valor associado) da coleção.

## <a name="syntax"></a>Sintaxe


```mof
uint32 KeyValueDelete(
  [in] string Key
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ no\]
</dt> <dd>

A chave a ser excluída.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                              |
| Namespace<br/>                | \\RDMs cimv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDSHCollection Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





