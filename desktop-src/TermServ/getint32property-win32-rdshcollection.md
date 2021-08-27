---
title: Método getint32property da classe Win32_RDSHCollection (Microsoft. Diagnostics. appanalysis. h)
description: Recupera um valor da propriedade Integer de um \_ objeto RDSHCollection do Win32.
ms.assetid: ab68f357-057d-4a36-ae39-f47198768a49
ms.tgt_platform: multiple
keywords:
- Método getint32property Serviços de Área de Trabalho Remota
- Método getint32property Serviços de Área de Trabalho Remota, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Serviços de Área de Trabalho Remota, método getint32property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61fb64c55a0b361ec4f3ca8528247f3884684b3321251c81594c3161c83a8c7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130711"
---
# <a name="getint32property-method-of-the-win32_rdshcollection-class"></a>Método getint32property da classe Win32 \_ RDSHCollection

Recupera um valor da propriedade Integer de um objeto [**\_ RDSHCollection do Win32**](win32-rdshcollection.md) .

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
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

## <a name="return-value"></a>Valor retornado

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                                 |
| Namespace<br/>                | \\RDMs CIMv2 \\ raiz<br/>                                                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Microsoft. Diagnostics. appanalysis. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RDSHCollection Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





