---
description: Não há suporte para a função RKeyPFXInstall.
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: Função RKeyPFXInstall (Rkeysvcc.h)
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
ms.openlocfilehash: f19a01e9132bf9c4b1e281a75b0e0d7a27b4f9c7f299eefdd47bef8d60daea97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900541"
---
# <a name="rkeypfxinstall-function"></a>Função RKeyPFXInstall

Não há suporte para a função **RKeyPFXInstall.**

**Windows Server 2003:** A **função RKeyPFXInstall** instala um certificado em um computador remoto. Observe que esse comportamento foi alterado com Windows Server 2003 com Service Pack 1 (SP1).

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

*hKeySvcCli* \[ Em\]
</dt> <dd>

Um [**handle KEYSVCC \_ HANDLE**](keysvcc-handle.md) aberto anteriormente por [**RKeyOpenKeyService**](rkeyopenkeyservice.md). O handle representa o computador remoto que receberá o certificado. Esse valor não pode ser **NULL.**

</dd> <dt>

*pPFX* \[ Em\]
</dt> <dd>

Um ponteiro para uma estrutura [**DE \_ BLOB KEYSVC**](keysvc-blob.md) que representa o certificado a ser instalado. O BLOB está no [*formato PKCS \# 12.*](../secgloss/p-gly.md)

</dd> <dt>

*pPassword* \[ Em\]
</dt> <dd>

Um ponteiro para uma estrutura [**KEYSVC \_ UNICODE \_ STRING**](keysvc-unicode-string.md) que representa a senha para o BLOB. Quando terminar de usar a senha, limpe a senha da memória chamando a [**função SecureZeroMemory.**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) Para obter mais informações sobre como proteger senhas, consulte [Tratamento de senhas](../secbp/handling-passwords.md).

</dd> <dt>

*ulFlags* \[ Em\]
</dt> <dd>

Sinalizadores que especificam as opções de instalação do certificado. Esse parâmetro pode ser um zero ou uma combinação dos valores a seguir.



| Valor                                                                                                                                                                                                                                     | Significado                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <dt>**CRYPT \_ EXPORTÁVEL**</dt><dt></dt> </dl>              | As chaves importadas são marcadas como exportáveis.<br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <dt>**CRYPT \_ MACHINE \_ KEYSET**</dt><dt></dt> </dl> | As chaves privadas são armazenadas no computador remoto e não no usuário atual.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, o valor de retorno será S \_ OK.

Se a função falhar, o valor de retorno será **um ULONG** que indica o erro.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Rkeysvcc.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 
