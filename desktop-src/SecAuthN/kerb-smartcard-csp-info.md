---
description: Contém informações sobre um CSP (provedor de serviços criptográficos) de cartão inteligente.
ms.assetid: b3e6722a-25dd-4137-b224-4082e846ddec
title: KERB_SMARTCARD_CSP_INFO estrutura
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
ms.openlocfilehash: 190c3e770a50acb7363fb10c469a7400831bc7b512d2b8158d687c83403b6df9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127336"
---
# <a name="kerb_smartcard_csp_info-structure"></a>Estrutura DE INFORMAÇÕES do CSP do KERB \_ SMARTCARD \_ \_

A **estrutura KERB \_ SMARTCARD \_ CSP \_ INFO** contém informações sobre um CSP (provedor de [*serviços criptográficos) de cartão*](../secgloss/c-gly.md) inteligente.

Essa estrutura não é declarada em um header público.

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

O tamanho, em bytes, dessa estrutura, incluindo todos os dados anexados.

</dd> <dt>

**MessageType**
</dt> <dd>

O tipo de mensagem que está sendo passada. Esse membro deve ser definido como 1.

</dd> <dt>

**Contextinformation**
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

**Keyspec**
</dt> <dd>

A chave privada a ser usada do contêiner de chave especificado no buffer **bBuffer.** A chave pode ser um dos valores a seguir, definidos em WinCrypt.h.



| Valor                                                                                                                                                                                                                   | Significado                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <dt>**AT \_ KEYEXCHANGE**</dt> <dt>1</dt> </dl> | A chave é uma chave de troca de chaves.<br/> |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <dt>**AT \_ ASSINATURA**</dt> <dt>2</dt> </dl>       | A chave é uma chave de assinatura.<br/>    |



 

</dd> <dt>

**nCardNameOffset**
</dt> <dd>

O número de caracteres no buffer **bBuffer** que precedem o nome do cartão inteligente nesse buffer.

> [!IMPORTANT]
> Se o nome do cartão inteligente não for fornecido, o buffer deverá conter uma cadeia de caracteres vazia.

 

</dd> <dt>

**nReaderNameOffset**
</dt> <dd>

O número de caracteres no buffer **bBuffer** que precedem o nome do leitor de cartão inteligente nesse buffer.

> [!IMPORTANT]
> Se o nome do leitor de cartão inteligente não for fornecido, o buffer deverá conter uma cadeia de caracteres vazia.

 

</dd> <dt>

**nContainerNameOffset**
</dt> <dd>

O número de caracteres no buffer **bBuffer** que precedem o nome do contêiner de chave nesse buffer. Essa cadeia de caracteres não pode estar vazia.

</dd> <dt>

**nCSPNameOffset**
</dt> <dd>

O número de caracteres no buffer **bBuffer** que precedem o nome do CSP nesse buffer.

</dd> <dt>

**bBuffer**
</dt> <dd>

Uma matriz de caracteres inicializados com um comprimento de `sizeof(DWORD)` . Esse buffer contém os nomes chamados pelos membros **nCardNameOffset**, **nReaderNameOffset**, **nContainerNameOffset** e **nCSPNameOffset,** bem como quaisquer dados adicionais fornecidos pelo CSP.

Todos os nomes que não são fornecidos devem ser representados nesse buffer por cadeias de caracteres vazias.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando essa estrutura é serializada, os membros da estrutura devem ser alinhados aos limites que são múltiplos de 2 bytes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LOGON DO \_ \_ CERTIFICADO KERB**](/windows/desktop/api/Ntsecapi/ns-ntsecapi-kerb_certificate_logon)
</dt> </dl>

 

 
