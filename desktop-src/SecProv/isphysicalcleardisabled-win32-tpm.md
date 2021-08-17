---
description: O método IsPhysicalClearDisabled da classe Win32 \_ TPM indica se somente o proprietário do dispositivo pode ser capaz de limpar o dispositivo.
ms.assetid: b87f1c4f-8735-45c5-9256-53dbb9579f95
title: Método IsPhysicalClearDisabled da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 7fd8841ad48480434fa1a686c2349e82d94eb01eda4f52084fd579cf67784870
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118891869"
---
# <a name="isphysicalcleardisabled-method-of-the-win32_tpm-class"></a>Método IsPhysicalClearDisabled da classe Win32 \_ TPM

O método **IsPhysicalClearDisabled** da classe [**Win32 \_ TPM**](win32-tpm.md) indica se somente o proprietário do dispositivo pode ser capaz de limpar o dispositivo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 IsPhysicalClearDisabled(
  [out] boolean IsPhysicalClearDisabled
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IsPhysicalClearDisabled* \[ fora\]
</dt> <dd>

Tipo: **booliano**

Se **for true**, somente o proprietário do dispositivo poderá limpar o dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **UInt32**

Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.

Os códigos de retorno comuns são listados abaixo.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Esse valor é redefinido como **false** no início de cada ciclo de inicialização.

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

 

 
