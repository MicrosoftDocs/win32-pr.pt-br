---
title: Método SetStringProperty da classe Win32_RDSHCollection (Certenroll.h)
description: Atualiza um valor da propriedade de cadeia de caracteres de um \_ objeto Win32 RDSHCollection.
ms.assetid: 6981b47a-5480-44f5-90e3-f64d439fa2aa
ms.tgt_platform: multiple
keywords:
- Método SetStringProperty Serviços de Área de Trabalho Remota
- Método SetStringProperty Serviços de Área de Trabalho Remota , Win32_RDSHCollection classe
- Win32_RDSHCollection classe Serviços de Área de Trabalho Remota , método SetStringProperty
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
ms.openlocfilehash: 87556f82f4004b6c7dbf194dfe38f47804d1fa07747ccb7e18d2b24a4a70f355
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987486"
---
# <a name="setstringproperty-method-of-the-win32_rdshcollection-class"></a>Método SetStringProperty da classe Win32 \_ RDSHCollection

Atualiza um valor da propriedade de cadeia de caracteres de um [**\_ objeto Win32 RDSHCollection.**](win32-rdshcollection.md)

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ Em\]
</dt> <dd>

A chave que identifica a propriedade a ser atualizada.

</dd> <dt>

*Valor* \[ Em\]
</dt> <dd>

O novo valor da propriedade.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                   |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                              |
| Namespace<br/>                | \\rdms CIMv2 \\ raiz<br/>                                                                |
| Cabeçalho<br/>                   | <dl> <dt>Certenroll.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





