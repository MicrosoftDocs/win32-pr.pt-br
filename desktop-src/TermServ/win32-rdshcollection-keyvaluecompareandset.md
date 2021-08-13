---
title: Método KeyValueCompareAndSet da classe Win32_RDSHCollection
description: Compara a chave especificada na coleção com um comparand; se eles corresponderem, a chave será definida como um novo valor. Se a chave não existir, o método inserirá a chave na coleção.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- Método KeyValueCompareAndSet Serviços de Área de Trabalho Remota
- Método KeyValueCompareAndSet Serviços de Área de Trabalho Remota , Win32_RDSHCollection classe
- Win32_RDSHCollection classe Serviços de Área de Trabalho Remota , método KeyValueCompareAndSet
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
ms.openlocfilehash: 52e1aaaf90313c8c1434a65c4ffd1045933ad503245f0dacbf78c2b7e1ca054a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422706"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a>Método KeyValueCompareAndSet da classe Win32 \_ RDSHCollection

Compara a chave especificada na coleção com um comparand; se eles corresponderem, a chave será definida como um novo valor. Se a chave não existir, o método inserirá a chave na coleção.

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

*Chave* \[ Em\]
</dt> <dd>

A chave a ser comparada.

</dd> <dt>

*NewValue* \[ Em\]
</dt> <dd>

O novo valor.

</dd> <dt>

*Comparand* \[ Em\]
</dt> <dd>

A cadeia de caracteres com a que comparar a chave.

</dd> <dt>

*InitialValue* \[ out\]
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
| Namespace<br/>                | Raiz \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





