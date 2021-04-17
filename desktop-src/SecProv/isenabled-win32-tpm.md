---
description: O método IsEnabled da classe Win32 \_ TPM indica se o dispositivo está habilitado. Esse valor pode ser alterado pelos métodos Enable e Disable.
ms.assetid: e1d5513f-33eb-49e3-9582-d6c103ca5d03
title: Método IsEnabled da classe Win32_Tpm
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
ms.openlocfilehash: d808bb68e53b1a24ff668d1b7a9680b5d57b5e9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782936"
---
# <a name="isenabled-method-of-the-win32_tpm-class"></a>Método IsEnabled da classe do \_ TPM do Win32

O método **IsEnabled** da classe [**Win32 \_ TPM**](win32-tpm.md) indica se o dispositivo está habilitado. Esse valor pode ser alterado pelos métodos [**Enable**](enable-win32-tpm.md) e [**Disable**](disable-win32-tpm.md) .

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsEnabled(
  [out] boolean IsEnabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsEnabled* \[ fora\]
</dt> <dd>

Tipo: **booliano**

Se for **true**, o dispositivo será habilitado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.

Os códigos de retorno comuns são listados abaixo.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

De acordo com a especificação de TCG (Trusted Computing Group) v 1.2, somente os comandos a seguir estão disponíveis quando o dispositivo está em um estado desativado.

-   \_CONTINUESELFTEST TPM
-   \_DSAP TPM
-   \_FLUSHSPECIFIC TPM
-   GetCapability do TPM \_
-   GetResult do TPM \_
-   Inicialização do TPM \_
-   \_OIAP TPM
-   \_oSAP TPM
-   \_OWNERSETDISABLE TPM
-   Redefinição de TPM \_ PCR \_
-   \_PHYSICALDISABLE TPM
-   \_PHYSICALENABLE TPM
-   \_PHYSICALSETDEACTIVATED TPM
-   Redefinição do TPM \_
-   \_SAVESTATE TPM
-   \_SELFTESTFULL TPM
-   Recurso do TPM \_
-   \_SHA1COMPLETE TPM
-   \_SHA1START TPM
-   \_SHA1UPDATE TPM
-   Inicialização do TPM \_
-   \_TAKEOWNERSHIP TPM
-   \_Identificador de término do TPM \_

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

[**Desabilitar**](disable-win32-tpm.md)
</dt> <dt>

[**Habilitar**](enable-win32-tpm.md)
</dt> </dl>

 

 
