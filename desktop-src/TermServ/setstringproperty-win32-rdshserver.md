---
title: Método SetStringProperty da classe Win32_RDSHServer (Certenroll.h)
description: Atualiza um valor de propriedade de cadeia de caracteres de um \_ objeto Win32 RDSHServer.
ms.assetid: 9a338872-27fc-4e37-afd6-20a42c7859e5
ms.tgt_platform: multiple
keywords:
- Método SetStringProperty Serviços de Área de Trabalho Remota
- Método SetStringProperty Serviços de Área de Trabalho Remota , Win32_RDSHServer classe
- Win32_RDSHServer classe Serviços de Área de Trabalho Remota , método SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2715271bcb73efd15acbef2097a29a978774e575a4fb115a9ef9e727e3efa91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349387"
---
# <a name="setstringproperty-method-of-the-win32_rdshserver-class"></a>Método SetStringProperty da classe \_ Win32 RDSHServer

Atualiza um valor de propriedade de cadeia de caracteres de um [**\_ objeto Win32 RDSHServer.**](win32-rdshserver.md)

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

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 





