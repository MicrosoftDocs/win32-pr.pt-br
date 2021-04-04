---
title: Método KeyValueGet da classe Win32_RDSHCollection
description: Recupera o valor associado à chave especificada na coleção.
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método KeyValueGet
- Método KeyValueGet Serviços de Área de Trabalho Remota, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Serviços de Área de Trabalho Remota, método KeyValueGet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5304cca379106094d4d00b9a0b5506c8df7075a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824318"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a>Método KeyValueGet da classe Win32 \_ RDSHCollection

Recupera o valor associado à chave especificada na coleção.

## <a name="syntax"></a>Sintaxe


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ no\]
</dt> <dd>

A chave que identifica o valor que você deseja recuperar.

</dd> <dt>

*Valor* \[ do fora\]
</dt> <dd>

Em caso de sucesso, retorna o valor associado à chave especificada.

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

 

 





