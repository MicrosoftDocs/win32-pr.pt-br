---
title: Estrutura de MCI_SYSINFO_PARMS (Mciapi. h)
description: A estrutura de parâmetros do sysinfo do MCI \_ \_ contém informações para o comando do sysinfo do MCI \_ .
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- Multimídia do Windows da estrutura de MCI_SYSINFO_PARMS
topic_type:
- apiref
api_name:
- MCI_SYSINFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf143bb0d895dc03df38bbb0a657467d506eac77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760818"
---
# <a name="mci_sysinfo_parms-structure"></a>Estrutura de parâmetros do \_ sysinfo do MCI \_

A estrutura de **\_ \_ parâmetros do sysinfo do MCI** contém informações para o comando do [**\_ sysinfo do MCI**](mci-sysinfo.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
  DWORD     dwNumber;
  UINT      wDeviceType;
} MCI_SYSINFO_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**lpstrReturn**
</dt> <dd>

Ponteiro para um buffer fornecido pelo usuário para a cadeia de caracteres de retorno. Ele também é usado para retornar um valor **DWORD** quando o sinalizador de quantidade do sysinfo do MCI \_ \_ é usado.

</dd> <dt>

**dwRetSize**
</dt> <dd>

Tamanho, em bytes, do buffer de retorno.

</dd> <dt>

**dwNumber**
</dt> <dd>

Número que indica a posição do dispositivo na tabela do dispositivo MCI ou na lista de dispositivos abertos se o \_ sinalizador de abertura do sysinfo do MCI \_ estiver definido.

</dd> <dt>

**wDeviceType**
</dt> <dd>

Tipo de dispositivo. Esse membro pode ser um dos valores listados em [tipos de dispositivo MCI](mci-device-types.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

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

[**SysInfo do MCI \_**](mci-sysinfo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

