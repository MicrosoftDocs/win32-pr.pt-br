---
description: O método IsOwnershipAllowed da classe Win32 \_ TPM indica se a capacidade de instalar um proprietário para o dispositivo é permitida.
ms.assetid: dfeb5afe-4169-470b-b5e4-cf1e5781271e
title: Método IsOwnershipAllowed da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnershipAllowed
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c818d5a4e4eb16ac637372f0c7ed0f2e9211ef88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164388"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a>Método IsOwnershipAllowed da classe Win32 \_ TPM

O método **IsOwnershipAllowed** da classe [**Win32 \_ TPM**](win32-tpm.md) indica se a capacidade de instalar um proprietário para o dispositivo é permitida.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsOwnershipAllowed* \[ fora\]
</dt> <dd>

Tipo: **booliano**

Se for **true**, a capacidade de instalar um proprietário para o dispositivo será permitida. Se **for false**, o método [**TakeOwnership**](takeownership-win32-tpm.md) falhará ao instalar um proprietário para o dispositivo.

Esse valor pode ser alterado com o método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) . O valor é redefinido como **true** depois que o método [**Clear**](clear-win32-tpm.md) é executado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.

Os códigos de retorno comuns são listados abaixo.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                      |
| Namespace<br/>                | \\MicrosoftTpm de \\ segurança \\ cimv2 raiz<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TPM do Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
