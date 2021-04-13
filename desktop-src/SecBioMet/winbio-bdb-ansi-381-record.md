---
title: Estrutura de WINBIO_BDB_ANSI_381_RECORD (WinBio \_ Types. h)
description: Contém informações sobre um único exemplo de impressão digital ou Palm de um usuário final.
ms.assetid: e0b32d05-3e96-4b42-9e18-57d10513f224
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_BDB_ANSI_381_RECORD
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_RECORD
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30af31d88349dbe02066f231cdff21293aebe90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369274"
---
# <a name="winbio_bdb_ansi_381_record-structure"></a>\_Estrutura de registro WINBIO BdB \_ ANSI \_ 381 \_

A estrutura de **\_ registro WINBIO BDB \_ ANSI \_ 381 \_** contém informações sobre um único exemplo de impressão digital ou Palm de um usuário final. Uma coleção dessas estruturas está incluída em cada estrutura [**de \_ cabeçalho WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-header.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_BDB_ANSI_381_RECORD {
  ULONG                    BlockLength;
  USHORT                   HorizontalLineLength;
  USHORT                   VerticalLineLength;
  WINBIO_BIOMETRIC_SUBTYPE Position;
  UCHAR                    CountOfViews;
  UCHAR                    ViewNumber;
  UCHAR                    ImageQuality;
  UCHAR                    ImpressionType;
  UCHAR                    Reserved;
} WINBIO_BDB_ANSI_381_RECORD;
```



## <a name="members"></a>Membros

<dl> <dt>

**BlockLength**
</dt> <dd>

Contém o número de bytes nessa estrutura mais o número de bytes de dados de imagem de exemplo.

</dd> <dt>

**HorizontalLineLength**
</dt> <dd>

Especifica o número de pixels em uma linha horizontal do exemplo.

</dd> <dt>

**VerticalLineLength**
</dt> <dd>

Especifica o número de pixels em uma linha vertical do exemplo.

</dd> <dt>

**Posição**
</dt> <dd>

Um valor de **\_ \_ subtipo biométrico WINBIO** que especifica o dedo ou o Palm usado para gerar o exemplo biométrico. Para obter mais informações, consulte Comentários.

</dd> <dt>

**CountOfViews**
</dt> <dd>

Isso deve ser definido como um (1);

</dd> <dt>

**ViewNumber**
</dt> <dd>

Isso deve ser definido como um (1);

</dd> <dt>

**ImageQuality**
</dt> <dd>

Reservado. Isso deve ser 254 (0xFE).

</dd> <dt>

**Impressiontype**
</dt> <dd>

Reservado.

</dd> <dt>

**Reserved**
</dt> <dd>

Reservado. Deve ser definido como zero (0).

</dd> </dl>

## <a name="remarks"></a>Comentários

O membro de *posição* especifica a área da mão ou o Palm usado para criar o exemplo biométrico. O Windows Biometric Framework (WBF) atualmente dá suporte apenas à captura de impressão digital e usa as constantes a seguir para representar informações de posição.

-   WINBIO \_ ANSI \_ 381 \_ pos \_ desconhecido
-   WINBIO \_ ANSI \_ 381 \_ pos \_ RH \_ Thumb
-   Dedo do índice de RH do WINBIO \_ ANSI \_ 381 \_ pos \_ \_ \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ \_ meio-dedo central de RH \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ - \_ anel de RH \_
-   WINBIO \_ ANSI \_ 381 \_ pos \_ \_ Little \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos de \_ LH \_ Thumb
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ index \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ do \_ meio- \_ dedo médio
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Ring \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ Little \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ pos \_ com \_ quatro \_ dedos
-   WINBIO \_ ANSI \_ 381 \_ pos \_ LH \_ quatro \_ dedos
-   WINBIO \_ ANSI \_ 381 \_ pos \_ dois \_ polegares

> [!IMPORTANT]
>
> Não tente validar o valor fornecido para o valor de *posição* . O serviço de biometria do Windows validará o valor fornecido antes de passá-lo para sua implementação. Se o valor for **WINBIO \_ subtipo \_ nenhuma \_ informação** ou **\_ subtipo WINBIO \_**, em seguida, valide quando apropriado.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> </dl>

 

 





