---
description: Gera um conjunto de chaves de sessão de protocolo de protocolo SSL (SSL).
ms.assetid: 88465f30-8591-411e-8618-8a381d4c22e9
title: Função SslGenerateSessionKeys (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateSessionKeys
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 3a9d7a25e5dd2035bd0b060ae11904e351489309b3a5e3c65c0e1582dce77500
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906168"
---
# <a name="sslgeneratesessionkeys-function"></a>Função SslGenerateSessionKeys

A função **SslGenerateSessionKeys** gera um conjunto de chaves de sessão de [*protocolo de protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslGenerateSessionKeys(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _Out_ NCRYPT_KEY_HANDLE  *phReadKey,
  _Out_ NCRYPT_KEY_HANDLE  *phWriteKey,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador para a instância do provedor de protocolo SSL.

</dd> <dt>

*hMasterKey* \[ no\]
</dt> <dd>

O identificador para o objeto de [*chave mestra*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*phReadKey* \[ fora\]
</dt> <dd>

Um ponteiro para o identificador de chave de leitura retornado.

</dd> <dt>

*phWriteKey* \[ fora\]
</dt> <dd>

Um ponteiro para o identificador de chave de gravação retornado.

</dd> <dt>

*pParameterList* \[ no\]
</dt> <dd>

Um ponteiro para uma matriz de buffers [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) que contém informações usadas como parte da operação de troca de chaves. O conjunto preciso de buffers depende do protocolo e do pacote de codificação usado. No mínimo, a lista conterá buffers que contêm os valores aleatórios de cliente e servidor fornecidos.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Esse parâmetro é reservado para uso futuro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                       | Descrição                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <dt>**Nte \_ SEM \_**</dt> <dt>0x8009000EL</dt> de memória </dl>         | Não há memória suficiente disponível para alocar os buffers necessários.<br/> |
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl>    | Um dos identificadores fornecidos não é válido.<br/>                     |
| <dl> <dt>**Nte \_ \_Parâmetro inválido**</dt> <dt>0x80090027L</dt> </dl> | O parâmetro *phReadKey* ou *phWriteKey* é nulo.<br/>            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

