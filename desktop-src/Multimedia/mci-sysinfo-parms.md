---
title: MCI_SYSINFO_PARMS (Mciapi.h)
description: A estrutura \_ MCI SYSINFO \_ PARMS contém informações para o comando \_ SYSINFO da MCI.
ms.assetid: 433649ed-7c00-440d-84f3-164949e01cc4
keywords:
- MCI_SYSINFO_PARMS estrutura Windows Multimídia
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
ms.openlocfilehash: 708d37f4d011997352a95b80dc80b8b9afd28730feeeb0e285a07d68c8c8eed5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117803126"
---
# <a name="mci_sysinfo_parms-structure"></a>Estrutura \_ PARMS MCI SYSINFO \_

A **estrutura \_ MCI SYSINFO \_ PARMS** contém informações para o [**comando \_ SYSINFO da MCI.**](mci-sysinfo.md)

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

**Dwcallback**
</dt> <dd>

A palavra de ordem baixa especifica um alça de janela usado para o sinalizador NOTIFY da \_ MCI.

</dd> <dt>

**lpstrReturn**
</dt> <dd>

Ponteiro para um buffer fornecido pelo usuário para a cadeia de caracteres de retorno. Ele também é usado para retornar um **valor DWORD** quando o sinalizador \_ QUANTITY da MCI SYSINFO \_ é usado.

</dd> <dt>

**dwRetSize**
</dt> <dd>

Tamanho, em bytes, do buffer de retorno.

</dd> <dt>

**dwNumber**
</dt> <dd>

Número que indica a posição do dispositivo na tabela do dispositivo MCI ou na lista de dispositivos abertos se o sinalizador OPEN \_ SYSINFO da MCI \_ estiver definido.

</dd> <dt>

**wDeviceType**
</dt> <dd>

Tipo de dispositivo. Esse membro pode ser um dos valores listados em [Tipos de Dispositivo MCI.](mci-device-types.md)

</dd> </dl>

## <a name="remarks"></a>Comentários

Ao atribuir dados aos membros dessa estrutura, defina os sinalizadores correspondentes no parâmetro *fdwCommand* da [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) para validar os membros.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mciapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Mci**](mci.md)
</dt> <dt>

[**Estruturas MCI**](mci-structures.md)
</dt> <dt>

[**MCI \_ SYSINFO**](mci-sysinfo.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

