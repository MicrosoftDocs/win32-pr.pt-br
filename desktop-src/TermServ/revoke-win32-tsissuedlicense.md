---
title: Método REVOKE da classe Win32_TSIssuedLicense
description: Revoga a Serviços de Área de Trabalho Remota licenças de acesso para cliente por dispositivo (RDS \ 160; CALs por dispositivo) que são representadas pelo \_ objeto TSIssuedLicense do Win32. Essa não é uma função estática.
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método REVOKE
- Método REVOKE Serviços de Área de Trabalho Remota, classe Win32_TSIssuedLicense
- Classe Win32_TSIssuedLicense Serviços de Área de Trabalho Remota, método REVOKE
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense.Revoke
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63993ede5346f5b3cb56fcfa458d4cdce7dd58b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645180"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a>Método REVOKE da classe Win32 \_ TSIssuedLicense

Revoga a Serviços de Área de Trabalho Remota licenças de acesso para cliente por dispositivo (RDS CALs por dispositivo) que são representadas pelo objeto [**\_ TSIssuedLicense do Win32**](win32-tsissuedlicense.md) . Essa não é uma função estática.

## <a name="syntax"></a>Sintaxe


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*RevokableCals* \[ fora\]
</dt> <dd>

Número de RDS CALs do mesmo tipo que o objeto atual que pode ser revogado.

</dd> <dt>

*NextRevokeAllowedOn* \[ fora\]
</dt> <dd>

Data em que o administrador pode tentar revogar licenças novamente. Esse parâmetro contém apenas dados válidos quando a chamada do método **REVOKE** falhou porque a contagem máxima de revogação foi atingida.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você deve ser um membro do grupo Administradores para chamar esse método.

Somente CALs por dispositivo RDS podem ser revogadas.

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                            |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**\_TSIssuedLicense Win32**](win32-tsissuedlicense.md)
</dt> </dl>

 

