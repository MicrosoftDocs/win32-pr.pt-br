---
title: Método GetProvisioningProperties da classe Win32_RDMSCollectionProperties
description: Recupera as propriedades de provisionamento da coleção de áreas de trabalho virtuais.
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método GetProvisioningProperties
- Método GetProvisioningProperties Serviços de Área de Trabalho Remota, classe Win32_RDMSCollectionProperties
- Classe Win32_RDMSCollectionProperties Serviços de Área de Trabalho Remota, método GetProvisioningProperties
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties.GetProvisioningProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ca58f82d2918441e5da3cf53d442497c1a6a2eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759945"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a>Método GetProvisioningProperties da classe Win32 \_ RDMSCollectionProperties

Recupera as propriedades de provisionamento da coleção de áreas de trabalho virtuais.

## <a name="syntax"></a>Sintaxe


```mof
uint32 GetProvisioningProperties(
  [out] string  PoolVhdType,
  [out] string  MasterVmLocation,
  [out] string  NamePrefix,
  [out] uint32  NameStartIndex,
  [out] string  LocalVmLocation,
  [out] string  LocalGoldVmLocation,
  [out] boolean RunFromSMB,
  [out] string  SMBLocation,
  [out] boolean SMBStreaming,
  [out] string  VmDomain,
  [out] string  VmOU,
  [out] string  ProductKey
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PoolVhdType* \[ fora\]
</dt> <dd>

Especifica o formato do VHD (disco rígido virtual) do pool de máquinas virtuais na coleção.

<dt>

Clone
</dt> <dd>

Um VHD clonado.

</dd> <dt>

DiffDisk
</dt> <dd>

Um VHD diferencial.

</dd> </dl> </dd> <dt>

*MasterVmLocation* \[ fora\]
</dt> <dd>

Recebe o caminho para a imagem da VM mestre.

</dd> <dt>

*NamePrefix* \[ fora\]
</dt> <dd>

Recebe o prefixo de nome a ser anexado ao início dos nomes de máquina virtual.

</dd> <dt>

*NameStartIndex* \[ fora\]
</dt> <dd>

Índice de início.

</dd> <dt>

*LocalVmLocation* \[ fora\]
</dt> <dd>

Recebe o caminho local para as máquinas virtuais nos servidores Hyper-V. Se esse parâmetro for definido como **nulo** ou estiver vazio, o diretório de máquina virtual padrão será usado.

</dd> <dt>

*LocalGoldVmLocation* \[ fora\]
</dt> <dd>

Recebe o caminho local para a imagem de VHD dourado quando o parâmetro *PoolVhdTpe* é definido como "DiffDisk". Se esse parâmetro for definido como **nulo** ou estiver vazio, o diretório de máquina virtual padrão será usado.

</dd> <dt>

*RunFromSMB* \[ fora\]
</dt> <dd>

Recebe um valor que indica se a coleção deve ser executada de um compartilhamento SMB (Server Message Block). **True** para executar as máquinas virtuais de um compartilhamento SBM; , **Falso**.

</dd> <dt>

*SMBLocation* \[ fora\]
</dt> <dd>

Recebe o caminho para o compartilhamento SMB se o compartilhamento SMB estiver habilitado.

</dd> <dt>

*SMBStreaming* \[ fora\]
</dt> <dd>

Recebe um valor que indica se o streaming SMB está habilitado. **True** se o compartilhamento SMB estiver habilitado; , **Falso**.

</dd> <dt>

*VmDomain* \[ fora\]
</dt> <dd>

Recebe o nome de domínio das máquinas virtuais na coleção.

</dd> <dt>

*VmOU* \[ fora\]
</dt> <dd>

Recebe a UO (unidade organizacional) Active Directory das máquinas virtuais na coleção.

</dd> <dt>

*ProductKey* \[ fora\]
</dt> <dd>

Recebe as chaves de produto do sistema operacional para as máquinas virtuais na coleção.

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

[**\_RDMSCollectionProperties Win32**](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





