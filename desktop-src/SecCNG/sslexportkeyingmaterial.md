---
description: Exporta o material de chave de acordo com o padrão RFC 5705.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: Função SslExportKeyingMaterial (Sslprovider.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslExportKeyingMaterial
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 39aaebba64f92794e179af95a5a175e2603fccc40410989cfcd427c6a7a1a88e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118906614"
---
# <a name="sslexportkeyingmaterial-function"></a>Função SslExportKeyingMaterial

Exporta o material de chave de acordo com o [padrão RFC 5705.](https://tools.ietf.org/html/rfc5705) Essa função usa a função pseudorandom TLS para produzir um buffer de byte de material de chave. Ele recebe uma referência ao segredo mestre, ao rótulo ASCII desambiguante, aos valores aleatórios do cliente e do servidor e, opcionalmente, aos dados de contexto do aplicativo.

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslExportKeyingMaterial(
  _In_     NCRYPT_PROV_HANDLE hSslProvider,
  _In_     NCRYPT_KEY_HANDLE  hMasterKey,
  _In_     PCHAR              sLabel,
  _In_     PBYTE              pbRandoms,
  _In_     DWORD              cbRandoms,
  _In_opt_ PBYTE              pbContextValue,
  _In_     WORD               cbContextValue,
  _Out_    PBYTE              pbOutput,
  _In_     DWORD              cbOutput,
  _In_     DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ Em\]
</dt> <dd>

O handle da instância do provedor de protocolo TLS.

</dd> <dt>

*hMasterKey* \[ Em\]
</dt> <dd>

O identificador do objeto de chave mestra que será usado para criar o material de chave para br exportado.

</dd> <dt>

*sLabel* \[ Em\]
</dt> <dd>

uma cadeia de caracteres de rótulo ASCII terminada em NUL. O Schannel removerá o caractere NUL de terminação antes de passá-lo para a função pseudorandom.

</dd> <dt>

*pbRandoms* \[ Em\]
</dt> <dd>

Um ponteiro para um buffer que contém uma *\_* concatenação dos valores *aleatórios \_* do cliente e do servidor da conexão TLS.

</dd> <dt>

*cbRandoms* \[ Em\]
</dt> <dd>

O comprimento, em bytes, do *buffer pbRandoms.*

</dd> <dt>

*pbContextValue* \[ in, opcional\]
</dt> <dd>

Um ponteiro para um buffer que contém o contexto do aplicativo. Se *pbContextValue* for **NULL,** *cbContextValue* deverá ser zero.

</dd> <dt>

*cbContextValue* \[ Em\]
</dt> <dd>

O comprimento, em bytes, do *buffer pbContextValue.*

</dd> <dt>

*pbOutput* \[ out\]
</dt> <dd>

O endereço de um buffer que recebe o material de chave exportado. O *parâmetro cbOutput* contém o tamanho desse buffer. Esse valor não pode ser **NULL.**

</dd> <dt>

*cbOutput* \[ Em\]
</dt> <dd>

O comprimento, em bytes, do *buffer pbOutput.* Deve ser maior que zero.

</dd> <dt>

*dwFlags* \[ Em\]
</dt> <dd>

Não usado. Deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for bem-sucedida, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferentes de zero.

Os possíveis códigos de retorno incluem, mas não estão limitados a, o seguinte.



| Valor/código de retorno                                                                                                                                                    | Descrição                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**NTE \_ HANDLE \_ INVÁLIDO**</dt> <dt>0x80090026L</dt> </dl> | Um dos alças fornecidos não é válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2016 somente aplicativos da área de trabalho\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




