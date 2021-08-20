---
title: MCI_OVLY_OPEN_PARMS (Mmsystem.h)
description: A estrutura MCI OVLY OPEN PARMS contém informações para o \_ \_ comando \_ MCI OPEN para \_ dispositivos de sobreposição de vídeo.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- MCI_OVLY_OPEN_PARMS estrutura Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_OVLY_OPEN_PARMS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2f13d0e9f8a7a4b9f5477459286bc56b9c98b1f9564e8432329681aeaef66d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118138271"
---
# <a name="mci_ovly_open_parms-structure"></a>Estrutura MCI \_ OVLY \_ OPEN \_ PARMS

A **estrutura MCI \_ OVLY \_ OPEN \_ PARMS** contém informações para o [**comando MCI \_ OPEN**](mci-open.md) para dispositivos de sobreposição de vídeo.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwStyle;
  DWORD       hWndParent;
} MCI_OVLY_OPEN_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dwcallback**
</dt> <dd>

A palavra de ordem baixa especifica um alça de janela usado para o sinalizador NOTIFY da \_ MCI.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Identificador retornado ao aplicativo.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Identificador de nome ou constante do tipo de dispositivo. (O nome do dispositivo normalmente é obtido do registro ou SYSTEM.INI arquivo.) Se esse membro for uma constante, ele poderá ser um dos valores listados em Tipos de [Dispositivo MCI.](mci-device-types.md)

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Nome do elemento do dispositivo (geralmente um caminho).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Alias de dispositivo opcional.

</dd> <dt>

**Dwstyle**
</dt> <dd>

Estilo da janela.

</dd> <dt>

**Hwndparent**
</dt> <dd>

Lidar com a janela pai.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

Você pode usar a estrutura [**MCI \_ OPEN \_ PARMS**](mci-open-parms.md) no lugar de **MCI \_ OVLY \_ OPEN \_ PARMS** se não estiver usando os membros de dados estendidos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Estruturas MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ OPEN**](mci-open.md)
</dt> <dt>

[**MCI \_ OPEN \_ PARMS**](mci-open-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

