---
title: Estrutura de WINBIO_BIR (WinBio \_ Types. h)
description: Representa um BIR (registro de informações biométricas).
ms.assetid: 39cfab34-0416-4897-bf95-a1b3c3a6a7a1
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_BIR
topic_type:
- apiref
api_name:
- WINBIO_BIR
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e422bbe59414d75541127b41e5e2cc1829adaaa7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105770462"
---
# <a name="winbio_bir-structure"></a>\_Estrutura WINBIO Bir

A estrutura **WINBIO \_ Bir** representa um Bir (registro de informações biométricas). O registro de informações contém cabeçalho, dados e blocos de assinatura.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_BIR {
  WINBIO_BIR_DATA HeaderBlock;
  WINBIO_BIR_DATA StandardDataBlock;
  WINBIO_BIR_DATA VendorDataBlock;
  WINBIO_BIR_DATA SignatureBlock;
} WINBIO_BIR;
```



## <a name="members"></a>Membros

<dl> <dt>

**HeaderBlock**
</dt> <dd>

Uma estrutura de [**\_ \_ dados WINBIO Bir**](winbio-bir-data.md) que contém o tamanho, em bytes, e o deslocamento do cabeçalho Bir. O cabeçalho contém informações que descrevem o conteúdo do registro de informações.

</dd> <dt>

**StandardDataBlock**
</dt> <dd>

Uma estrutura de [**\_ \_ dados WINBIO Bir**](winbio-bir-data.md) que contém o tamanho, em bytes, e o deslocamento de informações biométricas processadas ou não processados criadas pelo Windows Biometric Framework (WBF).

</dd> <dt>

**VendorDataBlock**
</dt> <dd>

Uma estrutura de [**\_ \_ dados WINBIO Bir**](winbio-bir-data.md) que contém o tamanho, em bytes, e o deslocamento de informações biométricas processadas ou não processados fornecidas por software e sensores do fornecedor.

</dd> <dt>

**SignatureBlock**
</dt> <dd>

Uma estrutura [**de \_ \_ dados WINBIO Bir**](winbio-bir-data.md) opcional que contém o tamanho, em bytes, e o deslocamento do Mac (código de autenticação de mensagem de assinatura digital) que pode ser usado para verificar a integridade do Bir. Se presente, a assinatura ou o MAC deve abranger o cabeçalho e os blocos de dados.

</dd> </dl>

## <a name="remarks"></a>Comentários

O uso de deslocamentos em vez de ponteiros permite uma fácil serialização do BIR e para uma tradução menos complicada entre os ambientes de 32 e 64 bits ou entre o modo de usuário e kernel.

O BIR é compatível com a CBEFF (estrutura de formato de intercâmbio biométrico) comum definida pelo NIST 6529-A.

Se essa estrutura contiver um valor *StandardDataBlock* , o parâmetro de *tipo* do cabeçalho especificado pelo parâmetro *HeaderBlock* deverá ser definido como **WINBIO \_ \_ \_ \_ tipo de formato ANSI 381**. Esse é o único formato de dados padrão com suporte da versão atual do Windows Biometric Framework.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ Bir \_ Data**](winbio-bir-data.md)
</dt> <dt>

[**\_cabeçalho WINBIO Bir \_**](winbio-bir-header.md)
</dt> </dl>

 

 





