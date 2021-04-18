---
title: comando sysinfo
description: O comando sysinfo recupera informações do sistema MCI. O comando sysinfo é um comando do sistema MCI; Ele é interpretado diretamente pelo MCI.
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- Multimídia do Windows de comando do sysinfo
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4751a5633462afe1ca8e8cd9abee1afeb16ac242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758300"
---
# <a name="sysinfo-command"></a>comando sysinfo

O comando sysinfo recupera informações do sistema MCI. O comando sysinfo é um comando do sistema MCI; Ele é interpretado diretamente pelo MCI.

Para enviar esse comando, chame a função [**mciSendString**](/previous-versions//dd757161(v=vs.85)) com o parâmetro *lpszCommand* definido da seguinte maneira.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("sysinfo %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpszDeviceID* 
</dt> <dd>

Identificador de um dispositivo ou tipo de dispositivo MCI. Se um tipo de dispositivo for especificado, ele deverá ser um nome de tipo de dispositivo MCI padrão, conforme listado no material de referência para o comando de [**capacidade**](capability.md) . Você pode especificar "All" quando o sinalizador especificado em *lpszRequest* permite essa possibilidade.

</dd> <dt>

*lpszRequest* 
</dt> <dd>

Um dos sinalizadores a seguir.



| Valor                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <dt>**instalar o**</dt> </dl>               | Retorna o nome listado no registro ou o arquivo de SYSTEM.INI usado para instalar o dispositivo aberto com o identificador de dispositivo especificado.<br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <dt>**quantidade**</dt> </dl>                        | Retorna o número de dispositivos MCI listados no registro ou o arquivo de SYSTEM.INI do tipo especificado no parâmetro *lpszDeviceID* . Esse identificador de dispositivo deve ser um nome de tipo de dispositivo MCI padrão. Quaisquer dígitos após o tipo de dispositivo são ignorados. A especificação de "All" para *lpszDeviceID* retorna o número total de dispositivos MCI no sistema.<br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <dt>**quantidade aberta**</dt> </dl>         | Retorna o número de dispositivos MCI abertos do tipo especificado em *lpszDeviceID*. Esse identificador de dispositivo deve ser um nome de tipo de dispositivo MCI padrão. A especificação de "All" para *lpszDeviceID* retorna o número total de dispositivos MCI abertos no sistema.<br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <dt>* * nome * índice * * *</dt> </dl>                | Retorna o nome de um dispositivo MCI. O identificador do dispositivo deve ser um nome de tipo de dispositivo MCI padrão. O *índice* varia de 1 até o número de dispositivos desse tipo. Se "All" for especificado para *lpszDeviceID*, os intervalos de *índice* de 1 para o número total de dispositivos no sistema.<br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <dt>***índice* de nome aberto**</dt> </dl> | Retorna o nome de um dispositivo MCI aberto. O identificador do dispositivo deve ser um nome de tipo de dispositivo MCI padrão. O *índice* varia de 1 até o número de dispositivos abertos desse tipo de dispositivo. Se "All" for especificado para *lpszDeviceID*, os intervalos de *índice* de 1 para o número total de dispositivos abertos no sistema.<br/>                                          |



 

</dd> <dt>

*lpszFlags* 
</dt> <dd>

Pode ser "Wait", "notificar" ou ambos. Para dispositivos de vídeo digital e VCR, o "teste" também pode ser especificado. Para obter mais informações sobre esses sinalizadores, consulte [os sinalizadores aguardar, notificar e testar](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="examples"></a>Exemplos

O comando a seguir retorna o número de dispositivos Open Wave-Audio.

``` syntax
sysinfo waveaudio quantity open
```

O comando a seguir retorna o nome (alias do dispositivo) do primeiro dispositivo Open Wave-Audio.

``` syntax
sysinfo waveaudio name 1 open
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/> |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Cadeias de caracteres de comando MCI](mci-command-strings.md)
</dt> <dt>

[**recursos**](capability.md)
</dt> </dl>

 

