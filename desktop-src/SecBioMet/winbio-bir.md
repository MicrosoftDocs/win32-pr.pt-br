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
ms.openlocfilehash: beb9e82a27717b33bcd0e06f5cd5bc23a3c43bc3a67cf70068f1a9eeb31b08bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911089"
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

uma estrutura de [**\_ \_ dados WINBIO BIR**](winbio-bir-data.md) que contém o tamanho, em bytes, e o deslocamento de informações biométricas processadas ou não processados criadas pelo Windows Biometric Framework (WBF).

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

o BIR é compatível com a estrutura de formato de Exchange biométrica comum (CBEFF) definida pelo NIST 6529-a.

Se essa estrutura contiver um valor *StandardDataBlock* , o parâmetro de *tipo* do cabeçalho especificado pelo parâmetro *HeaderBlock* deverá ser definido como **WINBIO \_ \_ \_ \_ tipo de formato ANSI 381**. esse é o único formato de dados padrão com suporte da versão atual do Windows Biometric Framework.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ Bir \_ Data**](winbio-bir-data.md)
</dt> <dt>

[**\_cabeçalho WINBIO Bir \_**](winbio-bir-header.md)
</dt> </dl>

 

 





