---
title: Estrutura de MCI_WAVE_OPEN_PARMS (Mciapi. h)
description: A \_ estrutura MCI \_ Open \_ parms de Wave contém informações para o \_ comando MCI Open para dispositivos de forma de onda-áudio.
ms.assetid: 2fc9383e-4610-4751-acad-b545dc6d8992
keywords:
- estrutura de MCI_WAVE_OPEN_PARMS Windows multimídia
topic_type:
- apiref
api_name:
- MCI_WAVE_OPEN_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 470b00bc818fb184174f27a8ff281359788f235ec7e31b899b051dc90423426c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783780"
---
# <a name="mci_wave_open_parms-structure"></a>\_Estrutura de \_ \_ parâmetros abertos do MCI Wave

A **estrutura \_ MCI \_ Open \_ parms de Wave** contém informações para o comando [**MCI \_ Open**](mci-open.md) para dispositivos de forma de onda-áudio.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR   dwCallback;
  MCIDEVICEID wDeviceID;
  LPCTSTR     lpstrDeviceType;
  LPCTSTR     lpstrElementName;
  LPCTSTR     lpstrAlias;
  DWORD       dwBufferSeconds;
} MCI_WAVE_OPEN_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**wDeviceID**
</dt> <dd>

Indentificador retornou ao aplicativo.

</dd> <dt>

**lpstrDeviceType**
</dt> <dd>

Nome ou identificador de constante do tipo de dispositivo. (O nome do dispositivo normalmente é obtido do registro ou do arquivo de SYSTEM.INI.) Esse membro pode ser um dos valores listados em [tipos de dispositivo MCI](mci-device-types.md).

</dd> <dt>

**lpstrElementName**
</dt> <dd>

Nome do elemento do dispositivo (geralmente um caminho).

</dd> <dt>

**lpstrAlias**
</dt> <dd>

Alias de dispositivo opcional.

</dd> <dt>

**dwBufferSeconds**
</dt> <dd>

Tamanho do buffer, em segundos.

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

Você pode usar a estrutura [**MCI \_ Open \_ parms**](mci-open-parms.md) em vez **de \_ \_ \_ parâmetros de abertura Wave MCI** se não estiver usando os membros de dados estendidos.

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

[**MCI \_ aberto**](mci-open.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**\_parâmetros de abertura do MCI \_**](mci-open-parms.md)
</dt> </dl>

 

