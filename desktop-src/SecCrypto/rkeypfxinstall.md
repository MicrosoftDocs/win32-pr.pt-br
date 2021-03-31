---
description: Não há suporte para a função RKeyPFXInstall.
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: Função RKeyPFXInstall (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyPFXInstall
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 4908b7224a02f5a28b876b1ff67cbcec7d23df5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920926"
---
# <a name="rkeypfxinstall-function"></a>Função RKeyPFXInstall

Não há suporte para a função **RKeyPFXInstall** .

**Windows Server 2003:** A função **RKeyPFXInstall** instala um certificado em um computador remoto. Observe que esse comportamento foi alterado com o Windows Server 2003 com Service Pack 1 (SP1).

## <a name="syntax"></a>Sintaxe


```C++
ULONG RKeyPFXInstall(
  _In_ KEYSVCC_HANDLE         hKeySvcCli,
  _In_ PKEYSVC_BLOB           pPFX,
  _In_ PKEYSVC_UNICODE_STRING pPassword,
  _In_ ULONG                  ulFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hKeySvcCli* \[ no\]
</dt> <dd>

Um identificador de [**\_ identificador KEYSVCC**](keysvcc-handle.md) aberto anteriormente pelo [**RKeyOpenKeyService**](rkeyopenkeyservice.md). O identificador representa o computador remoto que receberá o certificado. Esse valor não pode ser **nulo**.

</dd> <dt>

*pPFX* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ blob KEYSVC**](keysvc-blob.md) que representa o certificado a ser instalado. O BLOB está no formato [*PKCS \# 12*](../secgloss/p-gly.md) .

</dd> <dt>

*ppassword* \[ no\]
</dt> <dd>

Um ponteiro para uma estrutura de [**\_ cadeia de \_ caracteres Unicode KEYSVC**](keysvc-unicode-string.md) que representa a senha para o blob. Quando você terminar de usar a senha, limpe a senha da memória chamando a função [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) . Para obter mais informações sobre como proteger senhas, consulte [manipulando senhas](../secbp/handling-passwords.md).

</dd> <dt>

*ulFlags* \[ no\]
</dt> <dd>

Sinalizadores que especificam as opções de instalação do certificado. Esse parâmetro pode ser um zero ou uma combinação dos valores a seguir.



| Valor                                                                                                                                                                                                                                     | Significado                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <dt>**Cript \_ Exportável**</dt><dt></dt> </dl>              | As chaves importadas são marcadas como exportáveis.<br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <dt>**Cript \_ conjunto de \_ chaves da máquina**</dt><dt></dt> </dl> | As chaves privadas são armazenadas no computador remoto e não no usuário atual.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, o valor de retorno será S \_ OK.

Se a função falhar, o valor de retorno será um **ULONG** que indica o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 
