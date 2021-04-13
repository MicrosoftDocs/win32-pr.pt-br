---
title: Estrutura de MCI_INFO_PARMS (Mciapi. h)
description: A estrutura de parâmetros de informações do MCI \_ \_ contém informações para o comando de informações do MCI \_ .
ms.assetid: c64cff7d-a6d5-44b7-8cfb-9593f6328832
keywords:
- Multimídia do Windows da estrutura de MCI_INFO_PARMS
topic_type:
- apiref
api_name:
- MCI_INFO_PARMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d23221d140aaf093525691d7127c8466f392b95
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455955"
---
# <a name="mci_info_parms-structure"></a>Estrutura de parâmetros de \_ informações MCI \_

A estrutura de **\_ \_ parâmetros de informações do MCI** contém informações para o comando de [**\_ informações do MCI**](mci-info.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  DWORD_PTR dwCallback;
  LPTSTR    lpstrReturn;
  DWORD     dwRetSize;
} MCI_INFO_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**lpstrReturn**
</dt> <dd>

Buffer para cadeia de caracteres de retorno.

</dd> <dt>

**dwRetSize**
</dt> <dd>

Tamanho, em caracteres, da cadeia de caracteres de retorno.

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

[**informações do MCI \_**](mci-info.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

