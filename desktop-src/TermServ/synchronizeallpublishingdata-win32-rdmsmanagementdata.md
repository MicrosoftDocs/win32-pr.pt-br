---
title: Método SynchronizeAllPublishingData da classe Win32_RDMSManagementData
description: Sincroniza todos os dados de publicação para os serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 3a2135c3-26d6-4b6e-9680-f2d07f33ec05
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SynchronizeAllPublishingData
- Método SynchronizeAllPublishingData Serviços de Área de Trabalho Remota, classe Win32_RDMSManagementData
- Classe Win32_RDMSManagementData Serviços de Área de Trabalho Remota, método SynchronizeAllPublishingData
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizeAllPublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4db541954e1595c7b2fc8340f05a9415ad39b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644594"
---
# <a name="synchronizeallpublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a>Método SynchronizeAllPublishingData da classe Win32 \_ RDMSManagementData

Sincroniza todos os dados de publicação para os serviços de gerenciamento de Área de Trabalho Remota (RDMS).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SynchronizeAllPublishingData();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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

[**\_RDMSManagementData Win32**](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





