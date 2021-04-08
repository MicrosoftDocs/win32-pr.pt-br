---
title: Método QueryOfflineInformation da classe Win32_TSVm
description: Recupera as propriedades do VDS (servidor de área de trabalho virtual) atual, mas somente quando o servidor estiver offline.
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método QueryOfflineInformation
- Método QueryOfflineInformation Serviços de Área de Trabalho Remota, classe Win32_TSVm
- Classe Win32_TSVm Serviços de Área de Trabalho Remota, método QueryOfflineInformation
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824544"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a>Método QueryOfflineInformation da classe Win32 \_ TSVm

Recupera as propriedades do VDS (servidor de área de trabalho virtual) atual, mas somente quando o servidor estiver offline.

## <a name="syntax"></a>Sintaxe


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Criar* \[ fora\]
</dt> <dd>

Em caso de sucesso, retorna a versão de compilação do VDS.

</dd> <dt>

*CurrentVersion* \[ fora\]
</dt> <dd>

Em caso de sucesso, retorna a versão atual do VDS.

</dd> <dt>

*Installationtype* \[ fora\]
</dt> <dd>

Em caso de sucesso, retorna o tipo de instalação do VDS.

</dd> <dt>

*Edição do* \[ fora\]
</dt> <dd>

Em caso de sucesso, retorna a ID de edição do VDS.

</dd> <dt>

*SysPrepImageState* \[ fora\]
</dt> <dd>

Em caso de sucesso, retorna o estado da imagem de preparação do sistema do VDS.

</dd> <dt>

*Sysprepmode* \[ fora\]
</dt> <dd>

Em caso de sucesso, retorna o modo de preparação do sistema do VDS.

</dd> <dt>

*ProcArch* \[ fora\]
</dt> <dd>

Em caso de sucesso, retorna um valor que indica a arquitetura do processador.

<dt>

0
</dt> <dd>

x86

</dd> <dt>

1
</dt> <dd>

amd64

</dd> </dl> </dd> <dt>

*fIsVmbusCapable* \[ fora\]
</dt> <dd>

em caso de sucesso, indica se o sistema tem capacidade de VMBus.

</dd> <dt>

*fIsRdvIcInstalled* \[ fora\]
</dt> <dd>

Em caso de sucesso, indica se o RDVIC está instalado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                             |
| Namespace<br/>                | \\TerminalServices da CIMv2 raiz \\<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_TSVm Win32**](win32-tsvm.md)
</dt> </dl>

 

 





