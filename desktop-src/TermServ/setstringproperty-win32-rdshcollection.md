---
title: Método setstringproperty da classe Win32_RDSHCollection (CertEnroll. h)
description: Atualiza um valor de propriedade de cadeia de caracteres de um \_ objeto Win32 RDSHCollection.
ms.assetid: 6981b47a-5480-44f5-90e3-f64d439fa2aa
ms.tgt_platform: multiple
keywords:
- Método setstringproperty Serviços de Área de Trabalho Remota
- Método setstringproperty Serviços de Área de Trabalho Remota, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Serviços de Área de Trabalho Remota, método setstringproperty
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2606c195822432138ee67576db54f945c6834cfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769376"
---
# <a name="setstringproperty-method-of-the-win32_rdshcollection-class"></a>Método setstringproperty da classe Win32 \_ RDSHCollection

Atualiza um valor de propriedade de cadeia de caracteres de um objeto [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ no\]
</dt> <dd>

A chave que identifica a propriedade a ser atualizada.

</dd> <dt>

*Valor* \[ do no\]
</dt> <dd>

O novo valor da propriedade.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\RDMs CIMv2 \\ raiz<br/>                                                                |
| parâmetro<br/>                   | <dl> <dt>CertEnroll. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDSHCollection Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





