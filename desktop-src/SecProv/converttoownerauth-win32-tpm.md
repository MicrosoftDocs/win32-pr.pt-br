---
description: Converte uma entrada de senha fornecida pelo usuário em uma autorização de proprietário de 20 bytes que pode ser usada para interagir com o TPM. Métodos como TakeOwnership e ResetAuthLockOut exigem o valor de autorização do proprietário resultante.
ms.assetid: 69eed934-1668-495a-b5b7-cd4a87df1ab3
title: Método ConvertToOwnerAuth da classe Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ConvertToOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f3de5803d10458156fb453e964d782f7c9760333
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788094"
---
# <a name="converttoownerauth-method-of-the-win32_tpm-class"></a>Método ConvertToOwnerAuth da classe Win32 \_ TPM

O método **ConvertToOwnerAuth** da classe [**\_ TPM do Win32**](win32-tpm.md) converte uma entrada de senha fornecida pelo usuário em uma autorização de proprietário de 20 bytes que pode ser usada para interagir com o TPM. Métodos como [**TakeOwnership**](takeownership-win32-tpm.md) e [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md) exigem o valor de autorização do proprietário resultante.

O processo de conversão segue as especificações do [Trusted Computing Group](https://www.trustedcomputinggroup.org/).

## <a name="syntax"></a>Sintaxe


```mof
uint32 ConvertToOwnerAuth(
  [in]  string OwnerPassPhrase,
  [out] string OwnerAuth
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OwnerPassPhrase* \[ no\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres a ser convertida em um valor de autorização de proprietário. A cadeia de caracteres pode conter qualquer número de caracteres alfanuméricos.

</dd> <dt>

*OwnerAuth* \[ fora\]
</dt> <dd>

Tipo: **cadeia de caracteres**

Uma cadeia de caracteres derivada do parâmetro *OwnerPassPhrase* . Esse valor é um valor binário de 20 bytes codificado para uma cadeia de **caracteres com final de Base64 de** 28 bytes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **UInt32**

Todos os erros do TPM, bem como erros específicos para os serviços base do TPM, podem ser retornados.

As tabelas a seguir listam alguns dos códigos de retorno comuns.



| Código/valor de retorno                                                                                                                                 | Descrição                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0x0)</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Uma cadeia de caracteres codificada em UTF-16LE Unicode é convertida para o valor de autorização de proprietário do TPM de 20 bytes por meio do hash SHA-1 da representação binária da cadeia de caracteres. A terminação **nula** da cadeia de caracteres Unicode não está incluída no hash. Nenhum Salt é usado no hash SHA-1.

Por exemplo, para converter a frase secreta do proprietário do TPM "1Sample" em um valor de autorização de proprietário do TPM, o hash SHA-1 é obtido do seguinte fluxo de bytes:

`0x31 0x00 0x53 0x00 0x61 0x00 0x6D 0x00 0x70 0x00 0x6C 0x00 0x65 0x00`

Para converter uma senha de comprimento zero em um valor de autorização de proprietário, o hash SHA-1 é tirado do fluxo de bytes **nulo** .

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

[**TakeOwnership**](takeownership-win32-tpm.md)
</dt> </dl>

 

 
