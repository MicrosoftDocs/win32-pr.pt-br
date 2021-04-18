---
description: Define o comportamento de solicitação do repositório protegido sempre que ele exibe uma interface do usuário.
ms.assetid: 413bcb33-5fe9-4ba1-b65f-3e53a7cbf70c
title: Estrutura de PST_PROMPTINFO (Pstore. h)
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
ms.openlocfilehash: da499ea3d6f5037e9f1e745771112840a462f11d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771773"
---
# <a name="pst_promptinfo-structure"></a>Estrutura de PROMPTINFO de PST \_

\[O armazenamento protegido (Pstore) está disponível para uso no Windows Server 2003 e no Windows XP. Ele só está disponível para operações somente leitura no Windows Server 2008 e no Windows Vista, mas pode estar indisponível nas versões subsequentes. A Pstore usa uma implementação mais antiga da proteção de dados. Os desenvolvedores são altamente incentivados a aproveitar a proteção de dados mais forte fornecida pelas funções [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) e [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

Define o comportamento de solicitação do repositório protegido sempre que ele exibe uma interface do usuário.

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
| <span id="PST_PF_ALWAYS_SHOW"></span><span id="pst_pf_always_show"></span><dl> <dt>**PST \_ O PF \_ sempre \_ mostra**</dt> <dt>0x00000001</dt> </dl> | Solicita que o provedor mostre a caixa de diálogo de prompt para o usuário, mesmo que ele não seja necessário para esse acesso. <br/> |
| <span id="PST_PF_NEVER_SHOW"></span><span id="pst_pf_never_show"></span><dl> <dt>**PST \_ PF \_ nunca \_ Mostrar**</dt> <dt>0x00000002</dt> </dl>    | Não mostrar a caixa de diálogo de prompt para o usuário.<br/>                                                                 |



 

</dd> <dt>

**hwndApp**
</dt> <dd>

O identificador para a janela pai da interface do usuário. O membro **hwndApp** determina onde a interface do usuário é exibida. Se **NULL** for passado, a área de trabalho será considerada a janela pai.

</dd> <dt>

**szPrompt**
</dt> <dd>

A cadeia de caracteres do prompt.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Pstore. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**DeleteItem**](ipstore-deleteitem.md)
</dt> <dt>

[**OpenItem**](ipstore-openitem.md)
</dt> <dt>

[**ReadItem**](ipstore-readitem.md)
</dt> <dt>

[**WriteItem**](ipstore-writeitem.md)
</dt> </dl>

 

 
