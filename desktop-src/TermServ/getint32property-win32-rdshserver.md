---
title: Método GetInt32Property da classe Win32_RDSHServer (Microsoft.diagnostics.appanalysis.h)
description: Recupera um valor da propriedade integer de um objeto \_ Win32 RDSHServer.
ms.assetid: 4601e9cb-927b-4af8-a12b-09a8ca44c2f7
ms.tgt_platform: multiple
keywords:
- Método GetInt32Property Serviços de Área de Trabalho Remota
- Método GetInt32Property Serviços de Área de Trabalho Remota , Win32_RDSHServer classe
- Win32_RDSHServer classe Serviços de Área de Trabalho Remota , método GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba9114ca22a1052161000fcb05f38622ab9d210ec02b14715dad1bb85ce1365e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130667"
---
# <a name="getint32property-method-of-the-win32_rdshserver-class"></a>Método GetInt32Property da classe \_ Win32 RDSHServer

Recupera um valor da propriedade integer de um [**objeto \_ Win32 RDSHServer.**](win32-rdshserver.md)

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
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
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                                 |
| Namespace<br/>                | \\rdms CIMv2 \\ raiz<br/>                                                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Microsoft.diagnostics.appanalysis.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 





