---
title: Estrutura de WINBIO_REGISTERED_FORMAT (WinBio \_ Types. h)
description: Especifica um formato de dados registrado como um par de proprietário/formato.
ms.assetid: a178840e-81cc-4dd3-9d80-a181fa7fa888
keywords:
- API de Windows Biometric Framework de estrutura de WINBIO_REGISTERED_FORMAT
- Ponteiro de estrutura de PWINBIO_REGISTERED_FORMAT Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_REGISTERED_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f45293fe95627c7dfad4c9c51eb7fa74ad1738c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499384"
---
# <a name="winbio_registered_format-structure"></a>\_Estrutura de formato registrada WINBIO \_

A estrutura de **\_ \_ formato registrada WINBIO** especifica um formato de dados registrado como um par de proprietário/formato.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _WINBIO_REGISTERED_FORMAT {
  USHORT Owner;
  USHORT Type;
} WINBIO_REGISTERED_FORMAT, *PWINBIO_REGISTERED_FORMAT;
```



## <a name="members"></a>Membros

<dl> <dt>

**Proprietário**
</dt> <dd>

Um valor de proprietário atribuído do IBIA (International biometricity Industry).

</dd> <dt>

**Tipo**
</dt> <dd>

Um formato atribuído pelo proprietário.

</dd> </dl>

## <a name="remarks"></a>Comentários

Como o Windows atualmente dá suporte apenas a leitores de impressão digital, os valores a seguir devem ser usados na estrutura de **\_ \_ formato registrada WINBIO** .



| Constante                                    | Significado                                                                                                               |
|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| \_Proprietário do \_ formato ANSI 381 \_ \_ WINBIO<br/> | Comitê Internacional de INCITS (biometria) do Comitê Técnico de normas de tecnologia da informação (biométrica).<br/> |
| \_Tipo de formato WINBIO ANSI \_ 381 \_ \_<br/>  | Formato de intercâmbio de dados baseado em imagem de dedo ANSI INCITS 381.<br/>                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>WinBio \_ Types. h (inclui WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Estruturas de aplicativo cliente](client-application-structures.md)
</dt> <dt>

[**\_Constantes de formato WINBIO ANSI \_ 381 \_**](winbio-ansi-381-format-constants.md)
</dt> <dt>

[**\_Cabeçalho WINBIO BdB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-header.md)
</dt> <dt>

[**\_cabeçalho WINBIO Bir \_**](winbio-bir-header.md)
</dt> </dl>

 

 





