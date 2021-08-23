---
title: Estrutura de MCI_VCR_STATUS_PARMS (VCR. h)
description: A estrutura do parâmetro de \_ status do VCR MCI \_ \_ contém parâmetros para o comando de status do MCI \_ para gravadores de vídeo-fita.
ms.assetid: 5d7cbb64-a81d-4bdd-8f07-8c20dd7b9ef5
keywords:
- estrutura de MCI_VCR_STATUS_PARMS Windows multimídia
topic_type:
- apiref
api_name:
- MCI_VCR_STATUS_PARMS
api_location:
- Vcr.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8569a278f697ed816085c4fc8f313502d2994215519fb2452f82e63ce31a80cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783916"
---
# <a name="mci_vcr_status_parms-structure"></a>\_Estrutura de \_ parâmetros de status do VCR MCI \_

A estrutura do parâmetro de **\_ status do VCR \_ \_ MCI** contém parâmetros para o comando de [**\_ status do MCI**](mci-status.md) para gravadores de vídeo-fita.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct tagMCI_VCR_STATUS_PARMS {
  DWORD_PTR dwCallback;
  DWORD     dwReturn;
  DWORD     dwItem;
  DWORD     dwTrack;
  DWORD     dwNumber;
} MCI_VCR_STATUS_PARMS;
```



## <a name="members"></a>Membros

<dl> <dt>

**dwCallback**
</dt> <dd>

A palavra de ordem inferior Especifica um identificador de janela usado para o \_ sinalizador de notificação MCI.

</dd> <dt>

**dwReturn**
</dt> <dd>

Valor retornado pelo comando [**\_ status do MCI**](mci-status.md) . O valor de retorno varia de acordo com a consulta do comando. Para obter mais informações, consulte a descrição do [**comando \_ status do MCI**](mci-status-parms.md) .

</dd> <dt>

**dwItem**
</dt> <dd>

Tipo de informação solicitada.

</dd> <dt>

**dwTrack**
</dt> <dd>

Faixa de áudio ou vídeo que armazenará informações durante a próxima gravação. Esse membro é usado para retornar informações quando o [**comando \_ status do MCI**](mci-status-parms.md) questiona sobre o status de gravação de áudio ou vídeo.

</dd> <dt>

**dwNumber**
</dt> <dd>

Sintonizador lógico ao qual o canal atual está associado. Esse membro é usado para retornar informações quando o [**comando \_ status do MCI**](mci-status.md) questiona sobre o número do canal atual.

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

[**STATUS do MCI \_**](mci-status.md)
</dt> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> </dl>

 

