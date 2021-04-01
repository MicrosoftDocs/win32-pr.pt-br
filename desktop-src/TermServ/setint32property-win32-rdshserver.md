---
title: Método setint32property da classe Win32_RDSHServer
description: Atualiza um valor da propriedade Integer de um \_ objeto RDSHServer do Win32.
ms.assetid: fa8df023-120d-4174-adc1-868f08fdce56
ms.tgt_platform: multiple
keywords:
- Método setint32property Serviços de Área de Trabalho Remota
- Método setint32property Serviços de Área de Trabalho Remota, classe Win32_RDSHServer
- Classe Win32_RDSHServer Serviços de Área de Trabalho Remota, método setint32property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c22c8da9c046e0a42a6ec41f6ad5b3073c8d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644599"
---
# <a name="setint32property-method-of-the-win32_rdshserver-class"></a>Método setint32property da classe Win32 \_ RDSHServer

Atualiza um valor da propriedade Integer de um objeto [**\_ RDSHServer do Win32**](win32-rdshserver.md) .

## <a name="syntax"></a>Sintaxe


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
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
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDSHServer Win32**](win32-rdshserver.md)
</dt> </dl>

 

 





