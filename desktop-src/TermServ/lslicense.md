---
title: Estrutura LSLicense
description: Contém informações sobre uma licença de Serviços de Área de Trabalho Remota específica.
ms.assetid: 2c7f7b7a-e3b5-4f84-b49f-5f1d6960652d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota estrutura LSLicense
- Serviços de Área de Trabalho Remota de ponteiro de estrutura de LPLSLicense
topic_type:
- apiref
api_name:
- LSLicense
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3ea276b1b1217505a7bb44e1d70dd58d53eb57933d755ed9f79100abc177c3a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605409"
---
# <a name="lslicense-structure"></a>Estrutura LSLicense

Contém informações sobre uma licença de Serviços de Área de Trabalho Remota específica.

> [!Note]  
> Essa estrutura não está definida em nenhum arquivo de cabeçalho. Para usar essa estrutura, você deve defini-la por conta própria, conforme mostrado neste tópico.

 

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _LSLicense {
  DWORD dwVersion;
  DWORD dwLicenseId;
  DWORD dwKeyPackId;
  TCHAR szHWID[GUID_MAX_SIZE];
  TCHAR szMachineName[MAXCOMPUTERNAMELENGTH];
  TCHAR szUserName[MAXUSERNAMELENGTH];
  DWORD dwCertSerialLicense;
  DWORD dwLicenseSerialNumber;
  DWORD ftIssueDate;
  DWORD ftExpireDate;
  UCHAR ucLicenseStatus;
} LSLicense, *LPLSLicense;
```



## <a name="members"></a>Membros

<dl> <dt>

**DW**
</dt> <dd>

Versão da licença.

</dd> <dt>

**dwLicenseId**
</dt> <dd>

ID da licença.

</dd> <dt>

**dwKeyPackId**
</dt> <dd>

ID do [**LSKeyPack**](lskeypack.md) que contém a licença.

</dd> <dt>

**szHWID**
</dt> <dd>

ID de hardware do cliente de Conexão de Área de Trabalho Remota (RDC) que emitiu a licença.

</dd> <dt>

**szMachineName**
</dt> <dd>

Nome do cliente de Conexão de Área de Trabalho Remota (RDC) que emitiu a licença.

</dd> <dt>

**szUserName**
</dt> <dd>

Nome do usuário que emitiu a licença.

</dd> <dt>

**dwCertSerialLicense**
</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

**dwLicenseSerialNumber**
</dt> <dd>

Número de série da licença.

</dd> <dt>

**ftIssueDate**
</dt> <dd>

Data em que a licença foi emitida.

</dd> <dt>

**ftExpireDate**
</dt> <dd>

Data em que a licença irá expirar.

</dd> <dt>

**ucLicenseStatus**
</dt> <dd>

Status atual da licença.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dt>

[**TLSLicenseEnumBegin**](tlslicenseenumbegin.md)
</dt> <dt>

[**TLSLicenseEnumNext**](tlslicenseenumnext.md)
</dt> <dt>

[**TLSLicenseEnumEnd**](tlslicenseenumend.md)
</dt> </dl>

 

 





