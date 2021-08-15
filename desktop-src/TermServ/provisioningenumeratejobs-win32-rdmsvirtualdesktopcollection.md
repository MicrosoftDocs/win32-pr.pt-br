---
title: Método ProvisioningEnumerateJobs da classe Win32_RDMSVirtualDesktopCollection
description: Enumera trabalhos de provisionamento de área de trabalho virtual para esse serviço.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- Método ProvisioningEnumerateJobs Serviços de Área de Trabalho Remota
- Método ProvisioningEnumerateJobs Serviços de Área de Trabalho Remota , Win32_RDMSVirtualDesktopCollection classe
- Win32_RDMSVirtualDesktopCollection classe Serviços de Área de Trabalho Remota , método ProvisioningEnumerateJobs
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
ms.openlocfilehash: 5b24ef80acdb29c75327447f61db7dae1689a883f69c9e19ef199710de216fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118350218"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Método ProvisioningEnumerateJobs da classe Win32 \_ RDMSVirtualDesktopCollection

Enumera trabalhos de provisionamento de área de trabalho virtual para esse serviço.

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

*JobType* \[ Em\]
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

*CollectionAlias* \[ Em\]
</dt> <dd>

O alias da coleção de área de trabalho virtual a ser enumerada. O valor padrão para esse parâmetro é FALSE, que especifica que todos os trabalhos em execução devem ser enumerados.

</dd> <dt>

*JobGuids* \[ out\]
</dt> <dd>

Uma matriz que contém os **GUIDs de** trabalhos de provisionamento a enumerar.

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

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





