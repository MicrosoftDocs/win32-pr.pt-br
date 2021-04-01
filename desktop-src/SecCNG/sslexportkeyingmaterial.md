---
description: Exporta o material de chave de acordo com o padrão RFC 5705.
ms.assetid: 19624852-B1A6-4BB4-96AF-0457834DA294
title: Função SslExportKeyingMaterial (Sslprovider. h)
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
ms.openlocfilehash: 906a7535b297f309c0c8471843ce07f43a110a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103663357"
---
# <a name="sslexportkeyingmaterial-function"></a>Função SslExportKeyingMaterial

Exporta o material de chave de acordo com o [padrão RFC 5705](https://tools.ietf.org/html/rfc5705). Essa função usa a função TLS pseudoaleatória para produzir um buffer de bytes de material de chave. Ele usa uma referência para o segredo mestre, o rótulo ASCII de desambiguação, valores aleatórios de cliente e servidor e, opcionalmente, os dados de contexto do aplicativo.

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

*hSslProvider* \[ no\]
</dt> <dd>

O identificador da instância do provedor de protocolo TLS.

</dd> <dt>

*hMasterKey* \[ no\]
</dt> <dd>

O identificador do objeto de chave mestra que será usado para criar o material de chaveamento para br exportado.

</dd> <dt>

*sLabel* \[ no\]
</dt> <dd>

uma cadeia de caracteres de rótulo ASCII terminada por NUL. O Schannel removerá o caractere de terminação do NUL antes de passá-lo para a função pseudoaleatória.

</dd> <dt>

*pbRandoms* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém uma concatenação do *cliente \_ aleatório* e os *valores \_ aleatórios do servidor* da conexão TLS.

</dd> <dt>

*cbRandoms* \[ no\]
</dt> <dd>

O comprimento, em bytes, do buffer *pbRandoms* .

</dd> <dt>

*pbContextValue* \[ em, opcional\]
</dt> <dd>

Um ponteiro para um buffer que contém o contexto do aplicativo. Se *pbContextValue* for **nulo**, *cbContextValue* deverá ser zero.

</dd> <dt>

*cbContextValue* \[ no\]
</dt> <dd>

O comprimento, em bytes, do buffer *pbContextValue* .

</dd> <dt>

*pbOutput* \[ fora\]
</dt> <dd>

O endereço de um buffer que recebe o material de chave exportado. O parâmetro *cbOutput* contém o tamanho desse buffer. Esse valor não pode ser **nulo**.

</dd> <dt>

*cbOutput* \[ no\]
</dt> <dd>

O comprimento, em bytes, do buffer *pbOutput* . Deve ser maior que zero.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Não usado. Deve ser definido como zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.

Os códigos de retorno possíveis incluem, mas não se limitam a, o seguinte.



| Código/valor de retorno                                                                                                                                                    | Descrição                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl> | Um dos identificadores fornecidos não é válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

 




