---
title: Método SynchronizePublishingData da classe Win32_RDMSManagementData
description: Sincroniza o conjunto especificado de dados de publicação para os serviços de gerenciamento de Área de Trabalho Remota (RDMS).
ms.assetid: 0476ce12-9b08-418c-83c2-208275574f5b
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SynchronizePublishingData
- Método SynchronizePublishingData Serviços de Área de Trabalho Remota, classe Win32_RDMSManagementData
- Classe Win32_RDMSManagementData Serviços de Área de Trabalho Remota, método SynchronizePublishingData
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizePublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d389ad08d81f39cab45502a42f4ebd95e16f36c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369565"
---
# <a name="synchronizepublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a>Método SynchronizePublishingData da classe Win32 \_ RDMSManagementData

Sincroniza o conjunto especificado de dados de publicação para os serviços de gerenciamento de Área de Trabalho Remota (RDMS).

## <a name="syntax"></a>Sintaxe


```mof
uint32 SynchronizePublishingData(
  [in] string Context
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Contexto* \[ do no\]
</dt> <dd>

As informações de contexto dos dados de publicação a serem sincronizados.

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

[**\_RDMSManagementData Win32**](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





