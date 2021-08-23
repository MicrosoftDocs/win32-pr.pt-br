---
description: Define os dados a serem usados na verificação de Authenticode da Microsoft dos dados do item.
ms.assetid: 73c0e84f-7d59-4efa-927d-af8d7305bc9d
title: Estrutura de PST_AUTHENTICODEDATA (Pstore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_AUTHENTICODEDATA
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: abf5bc69fd36e45cc715b3805f5407e821cfc7efc7f6595bcfc9eab8d762b716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690856"
---
# <a name="pst_authenticodedata-structure"></a>Estrutura de AUTHENTICODEDATA de PST \_

\[o Armazenamento protegido (pstore) está disponível para uso no Windows Server 2003 e no Windows XP. ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Define os dados a serem usados na verificação de Authenticode da Microsoft dos dados do item.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD    cbSize;
  DWORD    dwModifiers;
  LPCWSTR  szRootCA;
  LPCWSTR  szIssuer;
  LPCWSTR  szPublisher;
  LPCWSTR  szProgramName;
} PST_AUTHENTICODEDATA, *PPST_AUTHENTICODE_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho desta estrutura.

</dd> <dt>

**dwModifiers**
</dt> <dd>

Um valor que identifica o modificador que um de uma cadeia de chamadores deve verificar.



| Valor                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PST_AC_SINGLE_CALLER"></span><span id="pst_ac_single_caller"></span><dl> <dt>**PST \_ \_ \_ Chamador único de AC**</dt> <dt>0</dt> </dl>           | Apenas um único nível na cadeia de chamadas para Pstore. O chamador passa a verificação de verificação. A imagem especificada é o chamador imediato e é um aplicativo (.exe).<br/>              |
| <span id="PST_AC_TOP_LEVEL_CALLER"></span><span id="pst_ac_top_level_caller"></span><dl> <dt>**PST \_ \_ \_ \_ Chamador 1 de nível superior de AC**</dt> <dt></dt> </dl> | O chamador de nível superior deve passar na verificação, mas pode haver DLLs intermediárias. A imagem especificada não é necessariamente o chamador imediato e é um aplicativo (.exe).<br/>           |
| <span id="PST_AC_IMMEDIATE_CALLER"></span><span id="pst_ac_immediate_caller"></span><dl> <dt>**PST \_ \_ \_ Chamador imediato de AC**</dt> <dt>2</dt> </dl>  | O chamador imediato deve passar na verificação, mas não precisa ser o processo de nível superior. A imagem especificada é o chamador imediato, e a imagem pode ser um aplicativo (.exe) ou uma DLL.<br/> |



 

</dd> <dt>

**szRootCA**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres larga que representa a AC (autoridade de certificação) raiz do certificado; Use **NULL** para usar qualquer AC disponível.

</dd> <dt>

**szIssuer**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres larga que representa a autoridade de certificação que emitiu o certificado; Use **NULL** para usar qualquer AC disponível.

</dd> <dt>

**szPublisher**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres larga que representa o fornecedor do software; Use **NULL** para usar qualquer AC disponível.

</dd> <dt>

**szProgramName**
</dt> <dd>

Um ponteiro para uma cadeia de caracteres larga que representa o nome do programa; Use **NULL** para usar qualquer AC disponível.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl> |



 

 
