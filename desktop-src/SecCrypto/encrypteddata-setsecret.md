---
description: Define o valor do segredo usado para derivar a chave de sessão criptográfica usada para criptografar e descriptografar dados.
ms.assetid: d940ae0b-a697-4529-b494-0051b9a6db5e
title: Método EncryptedData.SetSecret
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.SetSecret
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0e56bd490c4e665d900eb39fb57d09019ab4cfa3b1eb3ad06ad74cb4e83514ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117766441"
---
# <a name="encrypteddatasetsecret-method"></a>Método EncryptedData.SetSecret

\[CAPICOM é um componente somente de 32 bits que está disponível para uso nos seguintes sistemas operacionais: Windows Server 2008, Windows Vista e Windows XP. Em vez disso, use o PInvoke (Serviços de Invocação de Plataforma) para chamar as funções de API do Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) e [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para criptografar e descriptografar mensagens. Para obter informações sobre o PInvoke, consulte [Tutorial de invocação de plataforma.](https://msdn.microsoft.com/library/aa288468.aspx) O .NET e a CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) Parte 1 e .NET e CryptoAPI por meio de [P/Invoke:](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subseções da parte 2 de Estender a criptografia do .NET com [CAPICOM e P/Invoke](/previous-versions/ms867087(v=msdn.10)) também podem ser úteis.\]

O **método SetSecret** define o valor do segredo usado para derivar a chave de sessão criptográfica [*usada*](../secgloss/s-gly.md) para criptografar e descriptografar dados.

## <a name="syntax"></a>Sintaxe


```VB
EncryptedData.SetSecret( _
  ByVal newVal, _
  [ ByVal SecretType ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*newVal* \[ Em\]
</dt> <dd>

Uma cadeia de caracteres que contém um segredo usado para criar uma chave de criptografia de sessão.

</dd> <dt>

*SecretType* \[ in, opcional\]
</dt> <dd>

Um valor da [**enumeração CAPICOM \_ SECRET \_ TYPE**](capicom-secret-type.md) que indica o tipo de segredo usado para gerar a chave de sessão. O valor padrão é CAPICOM \_ SECRET \_ PASSWORD. Esse parâmetro pode ser o valor a seguir.



| Valor                                                                                                                                                                                        | Significado                                                         |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="CAPICOM_SECRET_PASSWORD"></span><span id="capicom_secret_password"></span><dl> <dt>**SENHA SECRETA DO \_ CAPICOM \_**</dt> </dl> | A chave de criptografia deve ser derivada de uma senha.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O segredo é usado para criar a chave de sessão para criptografia ou descriptografia. O mesmo segredo deve ser usado para ambas as operações. Se o segredo usado para criptografar dados for perdido, os dados criptografados não poderão ser descriptografados.

Se apropriado para seu aplicativo, considere usar [**CryptProtectMemory**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory) ou [**CryptProtectData**](/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata) para proteger o segredo antes e depois do uso. Limpe a memória associada ao segredo quando terminar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows Vista<br/>                                                               |
| Fim do suporte ao servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuível<br/>       | CAPICOM 2.0 ou posterior no Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objetos de criptografia**](cryptography-objects.md)
</dt> <dt>

[**Encrypteddata**](encrypteddata.md)
</dt> </dl>

 

 
