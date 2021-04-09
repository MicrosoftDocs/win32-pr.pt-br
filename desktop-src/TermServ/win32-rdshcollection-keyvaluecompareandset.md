---
title: Método KeyValueCompareAndSet da classe Win32_RDSHCollection
description: Compara a chave especificada na coleção com um termo; Se eles corresponderem, a chave será definida como um novo valor. Se a chave não existir, o método irá inserir a chave na coleção.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método KeyValueCompareAndSet
- Método KeyValueCompareAndSet Serviços de Área de Trabalho Remota, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Serviços de Área de Trabalho Remota, método KeyValueCompareAndSet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b90d703b40cf76f59cc3caf5d8f197f387cfe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824319"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a>Método KeyValueCompareAndSet da classe Win32 \_ RDSHCollection

Compara a chave especificada na coleção com um termo; Se eles corresponderem, a chave será definida como um novo valor. Se a chave não existir, o método irá inserir a chave na coleção.

## <a name="syntax"></a>Sintaxe


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ no\]
</dt> <dd>

A chave a ser comparada.

</dd> <dt>

*NewValue* \[ no\]
</dt> <dd>

O novo valor.

</dd> <dt>

*Termo* \[ no\]
</dt> <dd>

A cadeia de caracteres para comparar a chave.

</dd> <dt>

*Inicialvalue* \[ fora\]
</dt> <dd>

Em caso de êxito ou falha, contém o valor inicial da chave.

</dd> </dl>

## <a name="remarks"></a>Comentários

Observe que esse método pode recuperar o valor da chave e, como tal, encapsula a funcionalidade de [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).

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

 

 





