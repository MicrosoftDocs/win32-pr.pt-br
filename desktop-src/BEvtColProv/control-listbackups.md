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
ms.openlocfilehash: ba6a3f042a6bd8f01e4bede00e22bda95ca28ebe7cc2beb33a12c6b49deba6bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589116"
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

*OriginalTimestampLow* \[ out\]
</dt> <dd>

O timestamp de quando a configuração atual foi definida (se restaurada do backup, conterá o timestamp original). Essa é a parte baixa de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*OriginalTimestampHigh* \[ out\]
</dt> <dd>

O timestamp de quando a configuração atual foi definida (se restaurada do backup, conterá o timestamp original). Essa é a parte alta do [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*Arquivos* \[ out\]
</dt> <dd>

A lista de arquivos de backup disponíveis, na ordem dos mais novos para os mais antigos.

</dd> <dt>

*FilesTimestampLow* \[ out\]
</dt> <dd>

Para cada arquivo de backup, o timestamp de quando sua configuração foi definida. Essa é a parte baixa de [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> <dt>

*FilesTimestampHigh* \[ out\]
</dt> <dd>

Para cada arquivo de backup, o timestamp de quando sua configuração foi definida. Essa é a parte alta do [**FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                          |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                       |
| Namespace<br/>                | Root \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

