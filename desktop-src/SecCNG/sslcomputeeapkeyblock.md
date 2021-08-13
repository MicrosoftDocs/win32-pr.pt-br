---
description: Computa o bloco de chave usado pelo protocolo EAP (Extensible Authentication Protocol).
ms.assetid: 0f382668-6fc6-440f-ba61-70b1db0f3987
title: Função SslComputeEapKeyBlock (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeEapKeyBlock
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 48f657f565c239f797fd67b108ce3b18b692dfabc0248e1005465e9123ac492d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907167"
---
# <a name="sslcomputeeapkeyblock-function"></a>Função SslComputeEapKeyBlock

A função **SslComputeEapKeyBlock** computa o bloco de chave usado pelo EAP (Extensible Authentication Protocol).

## <a name="syntax"></a>Sintaxe


```C++
SECURITY_STATUS WINAPI SslComputeEapKeyBlock(
  _In_      NCRYPT_PROV_HANDLE hSslProvider,
  _In_      NCRYPT_KEY_HANDLE  hMasterKey,
  _In_      PBYTE              pbRandoms,
  _In_      DWORD              cbRandoms,
  _Out_opt_ PBYTE              pbOutput,
  _In_      DWORD              cbOutput,
  _Out_     DWORD              *pcbResult,
  _In_      DWORD              dwFlags
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hSslProvider* \[ no\]
</dt> <dd>

O identificador da instância do provedor de protocolo de protocolo de [*protocolo SSL*](/windows/desktop/SecGloss/s-gly) (SSL).

</dd> <dt>

*hMasterKey* \[ no\]
</dt> <dd>

O identificador do objeto de [*chave mestra*](/windows/desktop/SecGloss/m-gly) .

</dd> <dt>

*pbRandoms* \[ no\]
</dt> <dd>

Um ponteiro para um buffer que contém uma concatenação do cliente \_ aleatório e os \_ valores aleatórios do servidor da sessão SSL.

</dd> <dt>

*cbRandoms* \[ no\]
</dt> <dd>

O comprimento, em bytes, do buffer *pbRandoms* .

</dd> <dt>

*pbOutput* \[ out, opcional\]
</dt> <dd>

O endereço de um buffer que recebe o BLOB de chave. O parâmetro *cbOutput* contém o tamanho desse buffer. Se esse parâmetro for **NULL**, essa função coloca o tamanho necessário, em bytes, no **DWORD** apontado pelo parâmetro *pcbResult* .

</dd> <dt>

*cbOutput* \[ no\]
</dt> <dd>

O comprimento, em bytes, do buffer *pbOutput* .

</dd> <dt>

*pcbResult* \[ fora\]
</dt> <dd>

Um ponteiro para um valor **DWORD** que especifica o comprimento, em bytes, do hash gravado no buffer *pbOutput* .

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Defina como **\_ sinalizador de \_ servidor \_ de SSL NCRYPT** para indicar que esta é uma chamada de servidor.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a função for realizada com sucesso, ela retornará zero.

Se a função falhar, ela retornará um valor de erro diferente de zero.



| Código/valor de retorno                                                                                                                                                    | Descrição                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**Nte \_ \_Identificador inválido**</dt> <dt>0x80090026L</dt> </dl> | Um dos identificadores fornecidos não é válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>Sslprovider. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ncrypt.dll</dt> </dl>    |



 

