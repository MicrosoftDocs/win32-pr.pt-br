---
description: O método IsOwnerClearDisabled da classe Win32 \_ TPM indica se o proprietário do dispositivo está restrito à limpeza do dispositivo.
ms.assetid: 04f98e9b-c1a0-4828-b7cb-67b32d7470ea
title: Método IsOwnerClearDisabled da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnerClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 13e8b7de707cb1b1af4d4ccdb1208c6391e26987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800065"
---
# <a name="isownercleardisabled-method-of-the-win32_tpm-class"></a>Método IsOwnerClearDisabled da classe Win32 \_ TPM

O método **IsOwnerClearDisabled** da classe [**Win32 \_ TPM**](win32-tpm.md) indica se o proprietário do dispositivo está restrito à limpeza do dispositivo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsOwnerClearDisabled(
  [out] boolean IsOwnerClearDisabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsOwnerClearDisabled* \[ fora\]
</dt> <dd>

Tipo: **booliano**

Se for **true**, o proprietário do dispositivo não poderá limpar o dispositivo. Somente um usuário fisicamente presente pode ser capaz de limpar o dispositivo. Se for **false**, o proprietário do dispositivo poderá limpar o dispositivo.

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

 

 
