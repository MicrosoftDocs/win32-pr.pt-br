---
title: Método ProvisioningEnumerateJobs da classe Win32_RDMSVirtualDesktopCollection
description: Enumera os trabalhos de provisionamento de área de trabalho virtual para este serviço.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método ProvisioningEnumerateJobs
- Método ProvisioningEnumerateJobs Serviços de Área de Trabalho Remota, classe Win32_RDMSVirtualDesktopCollection
- Classe Win32_RDMSVirtualDesktopCollection Serviços de Área de Trabalho Remota, método ProvisioningEnumerateJobs
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa2b54a0599c2bbcaf6b0f9a9acb3ab3028389b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499781"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método ProvisioningEnumerateJobs da classe Win32 \_ RDMSVirtualDesktopCollection

Enumera os trabalhos de provisionamento de área de trabalho virtual para este serviço.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*JobType* \[ no\]
</dt> <dd>

Um inteiro que especifica o tipo de trabalho a ser enumerado.

Esse parâmetro pode ser definido como um dos seguintes valores:

<dt>

0
</dt> <dd>

Executando trabalhos

</dd> <dt>

1
</dt> <dd>

Trabalhos concluídos

</dd> </dl> </dd> <dt>

*CollectionAlias* \[ no\]
</dt> <dd>

O alias da coleção de áreas de trabalho virtuais a ser enumerada. O valor padrão para esse parâmetro é FALSE, que especifica que todos os trabalhos em execução devem ser enumerados.

</dd> <dt>

*JobGuids* \[ fora\]
</dt> <dd>

Uma matriz que contém os **GUIDs** de trabalhos de provisionamento a serem enumerados.

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

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





