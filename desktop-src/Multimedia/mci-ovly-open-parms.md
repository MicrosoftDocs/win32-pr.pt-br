---
title: Estrutura de MCI_OVLY_OPEN_PARMS (mmsystem. h)
description: A \_ estrutura MCI OVLY \_ Open \_ parms contém informações para o \_ comando MCI Open para dispositivos de sobreposição de vídeo.
ms.assetid: 1559ae40-4aa5-4dfc-b337-7b056c706b67
keywords:
- Multimídia do Windows da estrutura de MCI_OVLY_OPEN_PARMS
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
ms.openlocfilehash: 4e64b864b4b0366421828960504aff3f5a83836b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454606"
---
# <a name="mci_ovly_open_parms-structure"></a>\_Estrutura de \_ \_ parâmetros abertos do MCI OVLY

A estrutura **MCI \_ OVLY \_ Open \_ parms** contém informações para o comando [**MCI \_ Open**](mci-open.md) para dispositivos de sobreposição de vídeo.

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

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Identificador retornado ao aplicativo.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Nome ou identificador de constante do tipo de dispositivo. (O nome do dispositivo normalmente é obtido do registro ou do arquivo de SYSTEM.INI.) Se esse membro for uma constante, ele poderá ser um dos valores listados em [tipos de dispositivo MCI](mci-device-types.md).

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Nome do elemento do dispositivo (geralmente um caminho).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Alias de dispositivo opcional.

</dd> <dt>

**dwStyle**
</dt> <dd>

Estilo da janela.

</dd> <dt>

**hWndParent**
</dt> <dd>

Identificador da janela pai.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

Você pode usar a estrutura [**MCI \_ Open \_ parms**](mci-open-parms.md) no lugar do **MCI \_ OVLY \_ Open \_ parms** se não estiver usando os membros de dados estendidos.

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

[**MCI \_ aberto**](mci-open.md)
</dt> <dt>

[**\_parâmetros de abertura do MCI \_**](mci-open-parms.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

