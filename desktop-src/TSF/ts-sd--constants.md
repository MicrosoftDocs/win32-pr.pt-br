---
title: Constantes de TS_SD_ (Textstor. h)
description: As \_ constantes TS SD \_ \ descrevem os Estados de documento dinâmico usados por um aplicativo em tempo de execução.
ms.assetid: fb673e42-bee7-484e-872a-d709d5ca12f2
topic_type:
- apiref
api_name:
- TS_SD_READONLY
- TS_SD_LOADING
- TS_SD_MASKALL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565bc97b9fa2d1474f1ba36cd8137e63125541e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105761365"
---
# <a name="ts_sd_-constants"></a>Constantes de TS \_ SD \_ \*

As \_ constantes TS SD \_ \* descrevem os Estados de documento dinâmico usados por um aplicativo em tempo de execução.



| Constante/valor                                                                                                                                                                                                                                              | Descrição                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <dt>**TS \_ SD \_ ReadOnly**</dt> <dt>(0x1)</dt> </dl>                              | O documento é somente leitura e não pode ser modificado.<br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <dt>**TS \_ \_Carregamento de SD**</dt> <dt>(0x2)</dt> </dl>                                 | O documento está sendo carregado e pode estar incompleto.<br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <dt>**TS \_ SD \_ MASKALL**</dt> <dt>(TS \_ SD \_ ReadOnly de \| TS \_ SD \_ carregando)</dt> </dl> | O documento é somente leitura e está sendo carregado.<br/>       |



## <a name="remarks"></a>Comentários

O membro **dwDynamicFlags** da estrutura [de \_ status TS](/windows/desktop/api/Textstor/ns-textstor-ts_status) usa essas constantes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[STATUS de TS \_](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[TF \_ as \_ \* constantes do SD](tf-sd--constants.md)
</dt> </dl>

 

 





