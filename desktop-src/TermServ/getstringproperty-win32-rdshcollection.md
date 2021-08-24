---
title: Método GetStringProperty da classe Win32_RDSHCollection
description: Recupera um valor da propriedade de cadeia de caracteres de um objeto \_ Win32 RDSHCollection.
ms.assetid: 8e97cd91-0e45-4d87-acfb-ee7d70376ce0
ms.tgt_platform: multiple
keywords:
- Método GetStringProperty Serviços de Área de Trabalho Remota
- Método GetStringProperty Serviços de Área de Trabalho Remota , Win32_RDSHCollection classe
- Win32_RDSHCollection classe Serviços de Área de Trabalho Remota , método GetStringProperty
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
ms.openlocfilehash: 81aa383e339bda2620c4accf42f3cd810d867ae6f1e9c0d2716ed688583a1972
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771826"
---
# <a name="getstringproperty-method-of-the-win32_rdshcollection-class"></a>Método GetStringProperty da classe Win32 \_ RDSHCollection

Recupera um valor da propriedade de cadeia de caracteres de um [**objeto \_ Win32 RDSHCollection.**](win32-rdshcollection.md)

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ Em\]
</dt> <dd>

A chave que identifica a propriedade a ser recuperada.

</dd> <dt>

*Valor* \[ out\]
</dt> <dd>

Recebe o valor da propriedade recuperada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\rdms CIMv2 \\ raiz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





