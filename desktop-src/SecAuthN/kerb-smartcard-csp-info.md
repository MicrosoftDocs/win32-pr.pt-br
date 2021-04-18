---
description: Contém informações sobre um provedor de serviços de criptografia (CSP) de cartão inteligente.
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: Estrutura de KERB_SMARTCARD_CSP_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KERB_SMARTCARD_CSP_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 03b1a8084e291dde5a4f1f2017e4e97f57640bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752827"
---
# <a name="kerb_smartcard_csp_info-structure"></a>\_Estrutura de \_ informações do CSP do KERB SmartCard \_

A estrutura de **\_ informações do \_ CSP \_ do KERB SmartCard** contém informações sobre um CSP ( [*provedor de serviços de criptografia*](../secgloss/c-gly.md) ) de cartão inteligente.

Essa estrutura não é declarada em um cabeçalho público.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _KERB_SMARTCARD_CSP_INFO {
  DWORD dwCspInfoLen;
  DWORD MessageType;
  union {
    PVOID   ContextInformation;
    ULONG64 SpaceHolderForWow64;
  };
  DWORD flags;
  DWORD KeySpec;
  ULONG nCardNameOffset;
  ULONG nReaderNameOffset;
  ULONG nContainerNameOffset;
  ULONG nCSPNameOffset;
  TCHAR bBuffer;
} KERB_SMARTCARD_CSP_INFO, *PKERB_SMARTCARD_CSP_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCspInfoLen**
</dt> <dd>

O tamanho, em bytes, dessa estrutura, incluindo os dados anexados.

</dd> <dt>

**MessageType**
</dt> <dd>

O tipo de mensagem que está sendo passada. Esse membro deve ser definido como 1.

</dd> <dt>

**ContextInformation**
</dt> <dd>

Reservado.

</dd> <dt>

**SpaceHolderForWow64**
</dt> <dd>

Reservado.

</dd> <dt>

**sinalizadores**
</dt> <dd>

Reservado.

</dd> <dt>

**KeySpec**
</dt> <dd>

A chave privada a ser usada do contêiner de chave especificado no buffer **bBuffer**. A chave pode ser um dos seguintes valores, definidos em WinCrypt. h.



| Valor                                                                                                                                                                                                                   | Significado                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**Às \_ TROCA**</dt> de <dt>key1</dt> </dl> | A chave é uma chave de troca de chaves.<br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**Às \_ ASSINATURA**</dt> <dt>2</dt> </dl>       | A chave é uma chave de assinatura.<br/>    |



 

</dd> <dt>

**nCardNameOffset**
</dt> <dd>

O número de caracteres no buffer **bBuffer** que precede o nome do cartão inteligente nesse buffer.

> [!IMPORTANT]
> Se o nome do cartão inteligente não for fornecido, o buffer deverá conter uma cadeia de caracteres vazia.

 

</dd> <dt>

**nReaderNameOffset**
</dt> <dd>

O número de caracteres no buffer **bBuffer** que precede o nome do leitor de cartão inteligente nesse buffer.

> [!IMPORTANT]
> Se o nome do leitor de cartão inteligente não for fornecido, o buffer deverá conter uma cadeia de caracteres vazia.

 

</dd> <dt>

**nContainerNameOffset**
</dt> <dd>

O número de caracteres no buffer **bBuffer** que precede o nome do contêiner de chave nesse buffer. Esta cadeia de caracteres não pode ficar vazia.

</dd> <dt>

**nCSPNameOffset**
</dt> <dd>

O número de caracteres no buffer **bBuffer** que precede o nome do CSP nesse buffer.

</dd> <dt>

**bBuffer**
</dt> <dd>

Uma matriz de caracteres inicializada com um comprimento de `sizeof(DWORD)` . Esse buffer contém os nomes referenciados pelos membros **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset** e **nCSPNameOffset** , bem como quaisquer dados adicionais fornecidos pelo CSP.

Os nomes que não são fornecidos devem ser representados nesse buffer por cadeias de caracteres vazias.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando essa estrutura é serializada, os membros da estrutura devem ser alinhados aos limites que são múltiplos de 2 bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_logon do certificado KERB \_**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
