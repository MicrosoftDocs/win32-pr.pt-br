---
description: O método IsEnabled da classe Win32 \_ Tpm indica se o dispositivo está habilitado. Esse valor pode ser alterado pelos métodos Habilitar e Desabilitar.
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Método IsEnabled da classe Win32_Tpm classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 1d61c96d9c80ae77f9869261905fb93461530b452deaf7a4709b394623a3dfab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119667496"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a>Método IsEnabled da classe Win32 \_ Tpm

O **método IsEnabled** da classe [**Win32 \_ Tpm**](win32-tpm.md) indica se o dispositivo está habilitado. Esse valor pode ser alterado pelos [**métodos Habilitar**](enable-win32-tpm.md) [**e**](disable-win32-tpm.md) Desabilitar.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsEnabled* \[ out\]
</dt> <dd>

Tipo: **booliana**

Se **for true,** o dispositivo será habilitado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **uint32**

Todos os erros do TPM, bem como erros específicos dos Serviços Base do TPM, podem ser retornados.

Os códigos de retorno comuns são listados abaixo.



| Valor/código de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

De acordo com a especificação Trusted Computing Group (TCG) v1.2, somente os comandos a seguir estarão disponíveis quando o dispositivo estiver em um estado desativado.

-   TPM \_ ContinueSelfTest
-   \_DSAP do TPM
-   TPM \_ FlushSpecific
-   GetCapability do TPM \_
-   TPM \_ GetTestResult
-   TPM \_ Init
-   OIAP do TPM \_
-   TPM \_ OSAP
-   TPM \_ OwnerSetDisable
-   Redefinição \_ de PCR do TPM \_
-   TPM \_ PhysicalDisable
-   TPM \_ PhysicalEnable
-   TPM \_ PhysicalSetDeactivated
-   Redefinição \_ do TPM
-   TPM \_ SaveState
-   TPM \_ SelfTestFull
-   SetCapability do TPM \_
-   TPM \_ SHA1Complete
-   TPM \_ SHA1Start
-   TPM \_ SHA1Update
-   Inicialização \_ do TPM
-   Propriedade \_ do TPM
-   TPM \_ Terminate \_ Handle

arquivos Managed Object Format (MOF) contêm as definições para classes WMI (Instrumentação de Gerenciamento de Windows). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, [consulte Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                      |
| Namespace<br/>                | Segurança \\ RAIZ CIMV2 \\ \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Win32 \_ Tpm**](win32-tpm.md)
</dt> <dt>

[**Desabilitar**](disable-win32-tpm.md)
</dt> <dt>

[**Habilitar**](enable-win32-tpm.md)
</dt> </dl>

 

 
