---
title: Método SetProgramList da classe Win32_TSVirtualIP classe
description: Substitui a lista de programas que usam a virtualização de IP.
ms.assetid: 4137c9b0-5b4d-4ab6-af2e-2cd98ba53563
ms.tgt_platform: multiple
keywords:
- Método SetProgramList Serviços de Área de Trabalho Remota
- Método SetProgramList Serviços de Área de Trabalho Remota , Win32_TSVirtualIP classe
- Win32_TSVirtualIP classe Serviços de Área de Trabalho Remota , método SetProgramList
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetProgramList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22ac74ca1a718fe1ec3c561b70da935d00a15f1bcb040cb29464ed9b6e52195c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349602"
---
# <a name="setprogramlist-method-of-the-win32_tsvirtualip-class"></a>Método SetProgramList da classe \_ Win32 TSVirtualIP

Substitui a lista de programas que usam a virtualização de IP.

## <a name="syntax"></a>Sintaxe


```mof
unint32 SetProgramList(
  [in] string ProgramList[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ProgramList* \[ Em\]
</dt> <dd>

Tipo: cadeia **de caracteres \[ \]**

Uma matriz de cadeias de caracteres que contêm os nomes de caminho e arquivo dos programas que usam a virtualização de IP.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **unint32**

Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI. Consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md) para ver uma lista desses valores. O método retornará um erro se a configuração estiver sob controle de política de grupo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\CiMv2 \\ TerminalServices raiz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)
</dt> </dl>

 

 





