---
title: Método getstringproperty da classe Win32_RDSHCollection
description: Recupera um valor de propriedade da cadeia de caracteres de um \_ objeto RDSHCollection do Win32.
ms.assetid: 8e97cd91-0e45-4d87-acfb-ee7d70376ce0
ms.tgt_platform: multiple
keywords:
- Método getstringproperty Serviços de Área de Trabalho Remota
- Método getstringproperty Serviços de Área de Trabalho Remota, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Serviços de Área de Trabalho Remota, método getstringproperty
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1895f05317850374a4f4b24d407a4c4ace9c5db7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918138"
---
# <a name="getstringproperty-method-of-the-win32_rdshcollection-class"></a>Método getstringproperty da classe Win32 \_ RDSHCollection

Recupera um valor de propriedade da cadeia de caracteres de um objeto [**\_ RDSHCollection do Win32**](win32-rdshcollection.md) .

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ no\]
</dt> <dd>

A chave que identifica a propriedade a ser recuperada.

</dd> <dt>

*Valor* \[ do fora\]
</dt> <dd>

Recebe o valor da propriedade recuperada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs CIMv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDSHCollection Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





