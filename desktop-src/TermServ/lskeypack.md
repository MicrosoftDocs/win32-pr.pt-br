---
title: Estrutura LSKeyPack
description: Contém informações sobre um pacote de chaves de licenciamento Serviços de Área de Trabalho Remota específico.
ms.assetid: c26d27ee-7dd3-49f0-a79c-752d23693a2a
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota estrutura LSKeyPack
- Serviços de Área de Trabalho Remota de ponteiro de estrutura de LPLSKeyPack
topic_type:
- apiref
api_name:
- LSKeyPack
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2b1ac1f51e66a0a3c15c33f2535bc02f1fd3528f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919040"
---
# <a name="lskeypack-structure"></a>Estrutura LSKeyPack

Contém informações sobre um pacote de chaves de licenciamento Serviços de Área de Trabalho Remota específico.

> [!Note]  
> Essa estrutura não está definida em nenhum arquivo de cabeçalho. Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _LSKeyPack {
  DWORD dwVersion;
  UCHAR ucKeyPackType;
  TCHAR szCompanyName[256];
  TCHAR szKeyPackId[256];
  TCHAR szProductName[256];
  TCHAR szProductId[256];
  TCHAR szProductDesc[256];
  WORD  wMajorVersion;
  WORD  wMinorVersion;
  DWORD dwPlatformType;
  UCHAR ucLicenseType;
  DWORD dwLanguageId;
  UCHAR ucChannelOfPurchase;
  TCHAR szBeginSerialNumber[256];
  DWORD dwTotalLicenseInKeyPack;
  DWORD dwProductFlags;
  DWORD dwKeyPackId;
  UCHAR ucKeyPackStatus;
  DWORD dwActivateDate;
  DWORD dwExpirationDate;
  DWORD dwNumberOfLicenses;
} LSKeyPack, *LPLSKeyPack;
```



## <a name="members"></a>Membros

<dl> <dt>

**DW**
</dt> <dd>

Versão do pacote de chaves.

</dd> <dt>

**ucKeyPackType**
</dt> <dd>

Tipo de pacote de chaves.

</dd> <dt>

**szCompanyName**
</dt> <dd>

Nome da empresa que emitiu o pacote de chaves.

</dd> <dt>

**szKeyPackId**
</dt> <dd>

ID do pacote de chaves.

</dd> <dt>

**szProductName**
</dt> <dd>

Nome do produto ao qual este pacote de chaves pertence.

</dd> <dt>

**szProductId**
</dt> <dd>

ID do produto ao qual este pacote de chaves pertence.

</dd> <dt>

**szProductDesc**
</dt> <dd>

Descrição do produto ao qual este pacote de chaves pertence.

</dd> <dt>

**wMajorVersion**
</dt> <dd>

Versão principal do produto ao qual este pacote de chaves pertence.

</dd> <dt>

**wMinorVersion**
</dt> <dd>

Versão secundária do produto ao qual este pacote de chaves pertence.

</dd> <dt>

**dwPlatformType**
</dt> <dd>

Tipo de plataforma.

</dd> <dt>

**ucLicenseType**
</dt> <dd>

Tipo de licenças no pacote de chaves.

</dd> <dt>

**dwLanguageId**
</dt> <dd>

Identificação de idioma

</dd> <dt>

**ucChannelOfPurchase**
</dt> <dd>

Canal de compra.

</dd> <dt>

**szBeginSerialNumber**
</dt> <dd>

Número de série da primeira licença.

</dd> <dt>

**dwTotalLicenseInKeyPack**
</dt> <dd>

Número total de licenças no pacote de chaves.

</dd> <dt>

**dwProductFlags**
</dt> <dd>

Flags.

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

ID do pacote de chaves.

</dd> <dt>

**ucKeyPackStatus**
</dt> <dd>

Status do pacote de chaves.

</dd> <dt>

**dwActivateDate**
</dt> <dd>

Data de ativação do pacote de chaves.

</dd> <dt>

**dwExpirationDate**
</dt> <dd>

Data de validade do pacote de chaves.

</dd> <dt>

**dwNumberOfLicenses**
</dt> <dd>

Número de licenças.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md)
</dt> <dt>

[**TLSKeyPackEnumNext**](tlskeypackenumnext.md)
</dt> <dt>

[**TLSKeyPackEnumEnd**](tlskeypackenumend.md)
</dt> </dl>

 

 





