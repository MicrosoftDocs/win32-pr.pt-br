---
description: Baixa a assinatura do arquivo. cab, verifica as permissões associadas aos pacotes e as executa com base na autenticação.
ms.assetid: b86a8f39-73a1-4e17-ac83-9ed095de4922
title: Função DownloadJavaEX
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DownloadJavaEX
api_type:
- DllExport
api_location:
- Javacypt.dll
ms.openlocfilehash: 31371e91599d604db591ee3e921b42bc809aae21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811132"
---
# <a name="downloadjavaex-function"></a>Função DownloadJavaEX

Baixa a assinatura do arquivo. cab, verifica as permissões associadas aos pacotes e as executa com base na autenticação.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT WINAPI DownloadJavaEX(
  _In_ PALLOCATOR               Reserved,
  _In_ PCRYPT_PROVIDER_DATA     pProviderData,
  _In_ PJAVA_POLICY_PROVIDER    pJava,
  _In_ CRYPT_PROVIDER_FUNCTIONS *pFunctions,
  _In_ BOOL                     fCertificate,
  _In_ PJAVA_TRUST              pTrust
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Reservado* \[ para no\]
</dt> <dd>

Esse parâmetro é reservado.

</dd> <dt>

*pProviderData* \[ no\]
</dt> <dd>

Uma estrutura de [**\_ \_ dados de provedor cript**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_data) que contém dados de certificado, como permissões de arquivo e de zona.

</dd> <dt>

*pJava* \[ no\]
</dt> <dd>

Uma estrutura de [**\_ \_ provedor de política Java**](/previous-versions//bb432350(v=vs.85)) que contém dados relacionados ao provedor de política.

</dd> <dt>

*pFunctions* \[ no\]
</dt> <dd>

Uma estrutura de [**\_ \_ funções de provedor criptografada**](/windows/win32/api/wintrust/ns-wintrust-crypt_provider_functions) que contém uma lista de métodos para verificar objetos de certificado, assinaturas e políticas finais.

</dd> <dt>

*fCertificate* \[ no\]
</dt> <dd>

Se um certificado estiver presente, esse parâmetro será **true**. Caso contrário, será **false**.

</dd> <dt>

*pTrust* \[ no\]
</dt> <dd>

Uma estrutura de [**\_ confiança do Java**](/windows/desktop/api/Capi/ns-capi-java_trust) que contém informações de confiança, como permissão codificada, assinatura do codificador e código de política de retorno autêntico.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem sucedido, o valor de retorno será **S \_ OK**. Caso contrário, o valor de retorno será um código de erro.

## <a name="remarks"></a>Comentários

Esta função não tem biblioteca de importação ou arquivo de cabeçalho associado; Você deve chamá-lo usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|-----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Javacypt.dll</dt> </dl> |



 

 
