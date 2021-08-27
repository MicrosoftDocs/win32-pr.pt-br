---
title: Estrutura de MCI_VCR_SEEK_PARMS (VCR. h)
description: A estrutura de parâmetros de busca de VCR do MCI \_ \_ \_ contém parâmetros para o \_ comando MCI Seek para gravadores de vídeo-fita.
ms.assetid: 40a9cef0-abdb-4698-b11e-5c3f67ea846b
keywords:
- estrutura de MCI_VCR_SEEK_PARMS Windows multimídia
topic_type:
- apiref
api_name:
- MCI_VCR_SEEK_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee25352925681ef548310d9e009808499ce0a36f80472e50ee2a0daa71ed8dd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038196"
---
# <a name="mci_vcr_seek_parms-structure"></a>\_Estrutura de \_ parâmetros de busca de VCR do MCI \_

A estrutura de parâmetros de busca de VCR do MCI contém parâmetros para o comando [**MCI \_ Seek**](mci-seek.md) para gravadores de vídeo-fita. **\_ \_ \_**

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMCI_VCR_SEEK_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwTo;
  DWORD     dwMark;
  DWORD     dwAt;
} MCI_VCR_SEEK_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwTo**
</dt> <dd>

Posição para a qual buscar.

</dd> <dt>

**dwMark**
</dt> <dd>

Marca numerada a ser procurada.

</dd> <dt>

**dwAt**
</dt> <dd>

Hora em que a busca começa.

</dd> </dl>

## <a name="remarks"></a>Comentários

As posições são especificadas no formato de hora atual.

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VCR. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estruturas MCI**](mci-structures.md)
</dt> <dt>

[**busca de MCI \_**](mci-seek.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

