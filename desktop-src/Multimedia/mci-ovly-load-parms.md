---
title: Estrutura de MCI_OVLY_LOAD_PARMS (mmsystem. h)
description: A \_ estrutura de parâmetros de carga OVLY do MCI \_ \_ contém informações para o \_ comando de carregamento MCI para dispositivos de sobreposição de vídeo.
ms.assetid: 701c27da-72bf-493d-a679-9e0bd210215d
keywords:
- Multimídia do Windows da estrutura de MCI_OVLY_LOAD_PARMS
topic_type:
- apiref
api_name:
- MCI_OVLY_LOAD_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2029e92f7991f1ae5d8d0bdbabc76eef456a36ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008838"
---
# <a name="mci_ovly_load_parms-structure"></a>\_Estrutura de \_ parâmetros de carga OVLY MCI \_

A estrutura de **\_ \_ \_ parâmetros de carga OVLY do MCI** contém informações para o comando de [**\_ carregamento MCI**](mci-load.md) para dispositivos de sobreposição de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPCTSTR   lpfilename;
  RECT      rc;
} MCI_OVLY_LOAD_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**lpfilename**
</dt> <dd>

Nome do arquivo a ser carregado.

</dd> <dt>

**RC**
</dt> <dd>

Identifica a área do buffer de vídeo a ser atualizada. As estruturas [Rect](/previous-versions//ms536136(v=vs.85)) são tratadas de forma diferente no MCI do que em outras partes do Windows; no MCI, **RC. Right** contém a largura do retângulo e **RC. Bottom** contém sua altura.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estruturas MCI**](mci-structures.md)
</dt> <dt>

[**\_carga MCI**](mci-load.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[RECT](/previous-versions//ms536136(v=vs.85))
</dt> </dl>

 

