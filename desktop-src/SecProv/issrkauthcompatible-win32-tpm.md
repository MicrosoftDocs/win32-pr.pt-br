---
description: o método IsSrkAuthCompatible da classe Win32 \_ Tpm indica se a autorização de chave raiz do Armazenamento (SRK) é compatível com o valor esperado pelo Windows Vista.
ms.assetid: ce6d05b8-673a-40ab-a1d7-3fedfd099306
title: Método IsSrkAuthCompatible da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsSrkAuthCompatible
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 435829389749d7f7e81552aa88dd00aa211fd74ae079c93c97b5baff3c7a3c4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891847"
---
# <a name="issrkauthcompatible-method-of-the-win32_tpm-class"></a>Método IsSrkAuthCompatible da classe Win32 \_ TPM

o método **IsSrkAuthCompatible** da classe [**Win32 \_ Tpm**](win32-tpm.md) indica se a autorização de chave raiz do Armazenamento (SRK) é compatível com o valor esperado pelo Windows Vista.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsSrkAuthCompatible(
  [out] boolean IsSrkAuthCompatible
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsSrkAuthCompatible* \[ fora\]
</dt> <dd>

Tipo: **booliano**

Se **for true**, o valor de autorização de SRK terá um valor igual a zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.

Os códigos de retorno comuns são listados abaixo.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK do Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                            |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                      |
| Namespace<br/>                | \\MicrosoftTpm de \\ segurança \\ cimv2 raiz<br/>                                            |
| MOF<br/>                      | <dl> <dt>\_TPM. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TPM do Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
