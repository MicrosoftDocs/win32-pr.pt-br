---
title: Estrutura de MCI_VD_PLAY_PARMS (Mciapi. h)
description: A estrutura do MCI \_ \_ reproduzir \_ parâmetros de reprodução contém informações de posição e velocidade para o \_ comando MCI Play para dispositivos VIDEODISC.
ms.assetid: 9fa8418f-3f69-4a9c-b23e-7d2e2c75c7af
keywords:
- estrutura de MCI_VD_PLAY_PARMS Windows multimídia
topic_type:
- apiref
api_name:
- MCI_VD_PLAY_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62c2aef6915d1e3cc325d5b9f8e1c7fe176a878c2d84080b5f8a77eaf034afc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783861"
---
# <a name="mci_vd_play_parms-structure"></a>\_Estrutura de \_ parâmetros de reprodução de VD do MCI \_

A estrutura do **MCI \_ \_ reproduzir \_ parâmetros de reprodução** contém informações de posição e velocidade para o comando [**MCI \_ Play**](mci-play.md) para dispositivos VIDEODISC.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  DWORD     dwFrom;
  DWORD     dwTo;
  DWORD     dwSpeed;
} MCI_VD_PLAY_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwFrom**
</dt> <dd>

Posição da qual reproduzir.

</dd> <dt>

**dwTo**
</dt> <dd>

Posição para reprodução.

</dd> <dt>

**dwSpeed**
</dt> <dd>

Velocidade de reprodução em quadros por segundo.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

Você pode usar a estrutura de [**\_ \_ parâmetros de reprodução MCI**](mci-play-parms.md) em vez de parâmetros de reprodução de VD do MCI se não estiver usando os membros de dados estendidos. **\_ \_ \_**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mciapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCI**](mci.md)
</dt> <dt>

[**Estruturas MCI**](mci-structures.md)
</dt> <dt>

[**\_reprodução MCI**](mci-play.md)
</dt> <dt>

[**\_parâmetros de reprodução MCI \_**](mci-play-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

