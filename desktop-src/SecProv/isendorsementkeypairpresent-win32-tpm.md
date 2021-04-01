---
description: O método IsEndorsementKeyPairPresent da classe Win32 \_ TPM indica se o par de chaves de endosso existe no dispositivo.
ms.assetid: c36cd0b5-1ac2-4fcf-b140-c5ecb0b3b211
title: Método IsEndorsementKeyPairPresent da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEndorsementKeyPairPresent
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 63561a4971523fd1554e1d973861c3f0737df2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091790"
---
# <a name="isendorsementkeypairpresent-method-of-the-win32_tpm-class"></a>Método IsEndorsementKeyPairPresent da classe Win32 \_ TPM

O método **IsEndorsementKeyPairPresent** da classe [**Win32 \_ TPM**](win32-tpm.md) indica se o par de chaves de endosso existe no dispositivo. O par de chaves de endosso é necessário antes que o dispositivo possa ser proprietário. Esse par de chaves pode ser criado pelo método [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md) .

O dispositivo deve ser habilitado e ativado para que esse método seja bem sucedido. Para habilitar e ativar um dispositivo sem proprietário, consulte o método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) .

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsEndorsementKeyPairPresent(
  [out] boolean IsEndorsementKeyPairPresent
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsEndorsementKeyPairPresent* \[ fora\]
</dt> <dd>

Tipo: **booliano**

Se **for true**, o par de chaves de endosso existirá no dispositivo.

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
</dt> <dt>

[**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)
</dt> <dt>

[**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)
</dt> </dl>

 

 
