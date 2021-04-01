---
title: Estrutura de MCI_VCR_SETTUNER_PARMS (VCR. h)
description: A estrutura do MCI do \_ \_ setajuster de videocassetes \_ contém parâmetros para o \_ comando de setajuste MCI para gravadores de vídeo-fita.
ms.assetid: 8254b4c0-80bb-44e4-9f51-1d7434d3b08f
keywords:
- Multimídia do Windows da estrutura de MCI_VCR_SETTUNER_PARMS
topic_type:
- apiref
api_name:
- MCI_VCR_SETTUNER_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 891ddf3b4b3dcb9532a2431901b0b2b9d84b0e52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644725"
---
# <a name="mci_vcr_settuner_parms-structure"></a>\_Estrutura de \_ parâmetros de setajuster de VCR MCI \_

A estrutura do **MCI do \_ \_ setajuster \_ de videocassetes** contém parâmetros para o comando de [**\_ setajuste MCI**](mci-settuner.md) para gravadores de vídeo-fita.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMCI_VCR_SETTUNER_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwChannel;
  DWORD     dwNumber;
} MCI_VCR_SETTUNER_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwChannel**
</dt> <dd>

Novo número de canal.

</dd> <dt>

**dwNumber**
</dt> <dd>

O sintonizador lógico que o comando do [**MCI \_ setajuste**](mci-settuner.md) afeta.

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

[**setajuster do MCI \_**](mci-settuner.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

