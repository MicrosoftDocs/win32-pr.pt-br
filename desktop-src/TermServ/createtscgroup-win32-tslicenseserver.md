---
title: Método CreateTSCGroup da classe Win32_TSLicenseServer classe
description: CreateTSCGroup não está mais disponível para uso a partir Windows Server 2012.
ms.assetid: 31751da7-263b-4911-a328-246457a606f0
ms.tgt_platform: multiple
keywords:
- Método CreateTSCGroup Serviços de Área de Trabalho Remota
- Método CreateTSCGroup Serviços de Área de Trabalho Remota , Win32_TSLicenseServer classe
- Win32_TSLicenseServer classe Serviços de Área de Trabalho Remota , método CreateTSCGroup
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.CreateTSCGroup
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf363d86cf663a3f9b626d9586140eb4c00f86e9750070f8a2000149b655bb34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737866"
---
# <a name="createtscgroup-method-of-the-win32_tslicenseserver-class"></a>Método CreateTSCGroup da classe \_ Win32 TSLicenseServer

\[**CreateTSCGroup** não está mais disponível para uso desde Windows Server 2012.\]

Não há suporte para o método.

**Windows Server 2008 R2 e Windows Server 2008:** Cria o grupo local Computadores do Servidor de Terminal Área de Trabalho Remota servidor de licença.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateTSCGroup();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorna **WBEM \_ E NÃO TEM \_ \_ SUPORTE.**

**Windows Server 2008 R2 e Windows Server 2008:** Se o método for bem-sucedido, ele retornará zero. Se o método não for bem-sucedido, ele retornará um valor diferente de zero. Para ver uma lista de códigos de erro, consulte Serviços de Área de Trabalho Remota códigos de erro do provedor [WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do Microsoft Windows Software Development Kit (SDK). Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Fim do suporte ao cliente<br/>    | Nenhum compatível<br/>                                                                 |
| Fim do suporte ao servidor<br/>    | Windows Server 2008 R2<br/>                                                         |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> <dt>

[**IsTSCGroupPresent**](istscgrouppresent-win32-tslicenseserver.md)
</dt> </dl>

 

