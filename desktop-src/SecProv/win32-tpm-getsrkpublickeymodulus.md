---
description: Obtém o módulo da parte pública da chave raiz de armazenamento do TPM.
ms.assetid: 266AE378-8BF2-4F6E-A055-E15D95E218DC
title: 'Método Win32_Tpm:: GetSrkPublicKeyModulus'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkPublicKeyModulus
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6d78abb695f2a9bc9de3887c8128395c2403b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762901"
---
# <a name="win32_tpmgetsrkpublickeymodulus-method"></a>\_Método TPM:: GetSrkPublicKeyModulus do Win32

Obtém o módulo da parte pública da chave raiz de armazenamento do TPM.

Esse método só pode ser acessado por administradores locais.

## <a name="syntax"></a>Sintaxe


```C++
uint32 GetSrkPublicKeyModulus(
  [out] uint8 SrkPublicKeyModulus
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*SrkPublicKeyModulus* \[ fora\]
</dt> <dd>

Retorna uma matriz de 256 bytes que contém o módulo da parte pública da chave de raiz de armazenamento do TPM

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

 

 
