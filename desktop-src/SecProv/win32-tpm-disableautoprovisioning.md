---
description: Desabilita o provisionamento automático do TPM se ele estiver habilitado no momento.
ms.assetid: 30CC2581-9C16-4A11-92F1-625992F2AF20
title: Win32_Tpm::D método isableAutoProvisioning
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.DisableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5387e744ec5f02bf448a997cfe1c8c83342903a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756374"
---
# <a name="win32_tpmdisableautoprovisioning-method"></a>TPM do Win32 \_ : método de:D isableautoprovisioning

Desabilita o provisionamento automático do TPM se ele estiver habilitado no momento. A operação não terá efeito se o provisionamento automático já estiver desabilitado. Por padrão, o provisionamento automático está habilitado para o Windows 8 e o Windows Server 2012.

Esse método só pode ser acessado por administradores locais.

## <a name="syntax"></a>Sintaxe


```C++
uint32 DisableAutoProvisioning(
  [in, optional] BOOL OnlyForNextBoot
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OnlyForNextBoot* \[ em, opcional\]
</dt> <dd>

Se definido como **true**, o provisionamento automático será desabilitado apenas para a próxima inicialização. Se definido como **false** ou não for especificado, o provisionamento automático será permanentemente desabilitado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Todos os erros do TPM, bem como erros específicos para os [serviços base do TPM](../tbs/tbs-return-codes.md) , podem ser retornados.

Os códigos de retorno comuns são listados abaixo.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). Os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                      |
| Namespace<br/>                | \\\\.\\ \\MicrosoftTpm de \\ segurança \\ cimv2 raiz<br/>                                     |
| MOF<br/>                      | <dl> <dt>\_TPM. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TPM do Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
