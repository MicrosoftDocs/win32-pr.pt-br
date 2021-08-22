---
description: Define o comportamento de solicitação do Armazenamento Protegido sempre que ele exibe uma interface do usuário.
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: PST_PROMPTINFO (Pstore.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_PROMPTINFO
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: b127ae7156c97f1fad41dd99cb575228ac9934dfb75c2e3765f3de1fa38e0a93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386206"
---
# <a name="pst_promptinfo-structure"></a>Estrutura PST \_ PROMPTINFO

\[O Armazenamento (Pstore) está disponível para uso no Windows Server 2003 e Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e Windows Vista, mas pode não estar disponível nas versões subsequentes. O Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData.**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata)\]

Define o comportamento de solicitação do Armazenamento Protegido sempre que ele exibe uma interface do usuário.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD      cbSize;
  DWORD      dwPromptFlags;
  DWORD_PTR  hwndApp;
  LPCWSTR    szPrompt;
} PST_PROMPTINFO, *PPST_PROMPTINFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**cbSize**
</dt> <dd>

O tamanho desta estrutura.

</dd> <dt>

**dwPromptFlags**
</dt> <dd>

Este sinalizador é ignorado.



| Valor                                                                                                                                                                                                                                          | Significado                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <dt>**PST \_ PF \_ ALWAYS \_ SHOW**</dt> <dt>0x00000001</dt> </dl> | Solicita que o provedor mostre a caixa de diálogo de prompt para o usuário, mesmo que ela não seja necessária para esse acesso. <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <dt>**PST \_ PF \_ NUNCA \_ MOSTRAR**</dt> <dt>0X00000002</dt> </dl>    | Não mostre a caixa de diálogo de prompt para o usuário.<br/>                                                                 |



 

</dd> <dt>

**hwndApp**
</dt> <dd>

O alça para a janela pai da interface do usuário. O **membro hwndApp** determina onde a interface do usuário é exibida. Se **NULL** for passado, a área de trabalho será considerada a janela pai.

</dd> <dt>

**szPrompt**
</dt> <dd>

A cadeia de caracteres do prompt.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Deleteitem**](ipstore-deleteitem.md)
</dt> <dt>

[**OpenItem**](ipstore-openitem.md)
</dt> <dt>

[**Readitem**](ipstore-readitem.md)
</dt> <dt>

[**WriteItem**](ipstore-writeitem.md)
</dt> </dl>

 

 
