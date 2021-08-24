---
title: Estrutura de MCI_VCR_LIST_PARMS (VCR. h)
description: A estrutura de parâmetros da \_ lista de videocassetes MCI \_ \_ contém parâmetros para o comando de lista de MCI \_ para gravadores de vídeo-fita.
ms.assetid: 88725599-8057-4787-96e6-49b4a651c894
keywords:
- estrutura de MCI_VCR_LIST_PARMS Windows multimídia
topic_type:
- apiref
api_name:
- MCI_VCR_LIST_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8eeb74aeee254ab050d394dbf250c037d00d10d51fe872052dd5d36164b2c3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137977"
---
# <a name="mci_vcr_list_parms-structure"></a>\_Estrutura de \_ parâmetros da lista de VIDEOCASSETEs MCI \_

A estrutura de parâmetros da **\_ \_ lista \_ de videocassetes MCI** contém parâmetros para o comando de [**\_ lista de MCI**](mci-list.md) para gravadores de vídeo-fita.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMCI_VCR_LIST_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwNumber;
} MCI_VCR_LIST_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwReturn**
</dt> <dd>

Buffer para informações retornadas.

</dd> <dt>

**dwNumber**
</dt> <dd>

Número de entradas de áudio ou vídeo do VCR.

</dd> </dl>

## <a name="remarks"></a>Comentários

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

[**lista de MCI \_**](mci-list.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

