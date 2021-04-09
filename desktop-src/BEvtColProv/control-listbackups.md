---
description: Retorna a lista dos arquivos de configuração de backup salvos que podem ser restaurados.
ms.assetid: 9487c50e-ef3b-425f-92ef-0614290e9af4
ms.tgt_platform: multiple
title: Método ListBackups da classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ListBackups
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 858fb7ee38b7875426ae31172618ad8ac60510ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088884"
---
# <a name="listbackups-method-of-the-control-class"></a>Método ListBackups da classe Control

Retorna a lista dos arquivos de configuração de backup salvos que podem ser restaurados.

## <a name="syntax"></a>Sintaxe


```mof
void ListBackups(
  [out] Uint32 OriginalTimestampLow,
  [out] Uint32 OriginalTimestampHigh,
  [out] string Files[],
  [out] Uint32 FilesTimestampLow[],
  [out] Uint32 FilesTimestampHigh[]
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*OriginalTimestampLow* \[ fora\]
</dt> <dd>

O carimbo de data/hora de quando a configuração atual foi definida (se restaurada do backup, conterá o carimbo de data/hora original). Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*OriginalTimestampHigh* \[ fora\]
</dt> <dd>

O carimbo de data/hora de quando a configuração atual foi definida (se restaurada do backup, conterá o carimbo de data/hora original). Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*Arquivos* \[ do fora\]
</dt> <dd>

A lista de arquivos de backup disponíveis, na ordem do mais recente ao mais antigo.

</dd> <dt>

*FilesTimestampLow* \[ fora\]
</dt> <dd>

Para cada arquivo de backup, o carimbo de data/hora de quando sua configuração foi definida. Essa é a parte inferior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> <dt>

*FilesTimestampHigh* \[ fora\]
</dt> <dd>

Para cada arquivo de backup, o carimbo de data/hora de quando sua configuração foi definida. Essa é a parte superior do [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Raiz \\ do Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Controlo**](control.md)
</dt> </dl>

 

