---
description: Contém o cabeçalho do GRL (lista de revogação global).
ms.assetid: 806ae550-5106-47ec-8466-f967598d3e61
title: Estrutura de GRL_HEADER
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GRL_HEADER
api_type:
- NA
api_location: ''
ms.openlocfilehash: c20c9323ac627f9f1d6c63ae893d1633fb3cd96f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753842"
---
# <a name="grl_header-structure"></a>\_Estrutura do cabeçalho grl

Contém o cabeçalho do GRL (lista de revogação global).

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _GRL_HEADER {
  WCHAR    wszIdentifier[6];
  WORD     wFormatMajor;
  WORD     wFormatMinor;
  FILETIME CreationTime;
  DWORD    dwSequenceNumber;
  DWORD    dwForceRebootVersion;
  DWORD    dwForceProcessRestartVersion;
  DWORD    cbRevocationSectionOffset;
  DWORD    cRevokedKernelBinaries;
  DWORD    cRevokedUserBinaries;
  DWORD    cRevokedCertificates;
  DWORD    cTrustedRoots;
  DWORD    cbExtensibleSectionOffset;
  DWORD    cExtensibleEntries;
  DWORD    cbRenewalSectionOffset;
  DWORD    cRevokedKernelBinaryRenewals;
  DWORD    cRevokedUserBinaryRenewals;
  DWORD    cRevokedCertificateRenewals;
  DWORD    cbSignatureCoreOffset;
  DWORD    cbSignatureExtOffset;
} GRL_HEADER;
```



## <a name="members"></a>Membros

<dl> <dt>

**wszIdentifier**
</dt> <dd>

O identificador GRL. O valor é sempre L "MSGRL".

</dd> <dt>

**wFormatMajor**
</dt> <dd>

O número da versão principal. No momento, o valor deve ser 1.

</dd> <dt>

**wFormatMinor**
</dt> <dd>

O número da versão secundária. No momento, o valor deve ser zero.

</dd> <dt>

**CreationTime**
</dt> <dd>

Um valor **FILETIME** que especifica quando o arquivo foi criado.

</dd> <dt>

**dwSequenceNumber**
</dt> <dd>

O número de versão do GRL. No momento, o valor deve ser pelo menos 3

</dd> <dt>

**dwForceRebootVersion**
</dt> <dd>

Reservado.

</dd> <dt>

**dwForceProcessRestartVersion**
</dt> <dd>

Reservado.

</dd> <dt>

**cbRevocationSectionOffset**
</dt> <dd>

O deslocamento, em bytes, do início do GRL para a seção principal.

</dd> <dt>

**cRevokedKernelBinaries**
</dt> <dd>

O número de binários de kernel revogados listados no GRL.

</dd> <dt>

**cRevokedUserBinaries**
</dt> <dd>

O número de binários de modo de usuário revogados listados no GRL.

</dd> <dt>

**cRevokedCertificates**
</dt> <dd>

O número de certificados revogados listados no GRL.

</dd> <dt>

**cTrustedRoots**
</dt> <dd>

O número de raízes confiáveis listadas no GRL.

</dd> <dt>

**cbExtensibleSectionOffset**
</dt> <dd>

O deslocamento, em bytes, do início do GRL para a seção extensível.

</dd> <dt>

**cExtensibleEntries**
</dt> <dd>

O número de entradas na seção extensível.

</dd> <dt>

**cbRenewalSectionOffset**
</dt> <dd>

O deslocamento, em bytes, do início do GRL para a seção renovações.

</dd> <dt>

**cRevokedKernelBinaryRenewals**
</dt> <dd>

O número de renovações binárias de kernel listadas no GRL.

</dd> <dt>

**cRevokedUserBinaryRenewals**
</dt> <dd>

O número de renovações binárias de modo de usuário listadas no GRL.

</dd> <dt>

**cRevokedCertificateRenewals**
</dt> <dd>

O número de renovações de certificado listadas no GRL.

</dd> <dt>

**cbSignatureCoreOffset**
</dt> <dd>

O deslocamento, em bytes, do início do GRL para a assinatura da seção principal.

</dd> <dt>

**cbSignatureExtOffset**
</dt> <dd>

O deslocamento, em bytes, do início do GRL para a assinatura da seção extensível.

</dd> </dl>

## <a name="remarks"></a>Comentários

Todos os inteiros no GRL têm ordenação de byte little-endian. Todas as estruturas são alinhadas a limites de 1 byte.

Essa estrutura não é declarada em um cabeçalho do SDK. Para usar essa estrutura, adicione a declaração mostrada aqui ao seu código-fonte.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Revogação de certificado OPM](opm-certificate-revocation.md)
</dt> <dt>

[Estruturas OPM](opm-structures.md)
</dt> </dl>

 

 




