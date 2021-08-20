---
title: MCI_SYSINFO comando (Mmsystem.h)
description: O comando \_ SYSINFO da MCI recupera informações sobre dispositivos MCI.
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- MCI_SYSINFO comando Windows Multimídia
topic_type:
- apiref
api_name:
- MCI_SYSINFO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc308846da87053400ce04974677e51bb82c4c38356260485685e60c421606
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986127"
---
# <a name="mci_sysinfo-command"></a>Comando \_ SYSINFO da MCI

O comando \_ SYSINFO da MCI recupera informações sobre dispositivos MCI. A MCI dá suporte a esse comando diretamente em vez de passá-lo para o dispositivo. Qualquer aplicativo MCI pode usar esse comando. As informações de cadeia de caracteres são retornadas no buffer fornecido pelo aplicativo apontado pelo membro **lpstrReturn** da estrutura identificada por *lpSysInfo*. As informações numéricas são retornadas como **um valor DWORD** colocado no buffer fornecido pelo aplicativo. O **membro dwRetSize** especifica o comprimento do buffer.

Para enviar esse comando, chame a [**função mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SYSINFO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_SYSINFO_PARMS) lpSysInfo
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*
</dt> <dd>

Identificador de dispositivo do dispositivo MCI que deve receber a mensagem de comando.

</dd> <dt>

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*Dwflags*
</dt> <dd>

Um ou mais dos seguintes sinalizadores padrão e específicos de comando:

</dd> <dt>

<span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>MCI \_ SYSINFO \_ INSTALLNAME
</dt> <dd>

Obtém o nome (listado no registro ou no arquivo SYSTEM.INI) usado para instalar o dispositivo.

</dd> <dt>

<span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>NOME \_ SYSINFO DA MCI \_
</dt> <dd>

Obtém um nome de dispositivo correspondente ao número de dispositivo especificado no **membro dwNumber** da estrutura identificada por **lpSysInfo**. Se o sinalizador OPEN \_ SYSINFO da MCI \_ estiver definido, a MCI retornará os nomes dos dispositivos abertos.

</dd> <dt>

<span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>MCI \_ SYSINFO \_ OPEN
</dt> <dd>

Obtém a quantidade ou o nome dos dispositivos abertos.

</dd> <dt>

<span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>QUANTIDADE \_ DE SYSINFO DA MCI \_
</dt> <dd>

Obtém o número de dispositivos do tipo especificado listados no Registro ou na seção mci do \[ \] arquivo SYSTEM.INI dados. Se o sinalizador OPEN \_ SYSINFO da MCI \_ estiver definido, o número de dispositivos abertos será retornado.

</dd> <dt>

<span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*
</dt> <dd>

Ponteiro para uma [**estrutura \_ MCI SYSINFO \_ PARMS.**](mci-sysinfo-parms.md)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="remarks"></a>Comentários

O **membro wDeviceType** da estrutura identificada por *lpSysInfo* é usado para indicar o tipo de dispositivo da consulta. Se o *parâmetro wDeviceID* estiver definido como MCI ALL DEVICE ID, ele substituirá o valor \_ de \_ \_ **wDeviceType**. Para ver uma lista de tipos de dispositivo, consulte [Tipos de dispositivo MCI](mci-device-types.md).

Os valores retornados por inteiro são valores **DWORD** retornados no buffer apontado pelo membro **lpstrReturn** da estrutura identificada por *lpSysInfo*.

Os valores retornados da cadeia de caracteres são cadeias de caracteres terminadas em nulo retornadas no buffer apontado pelo membro **lpstrReturn** da estrutura identificada por *lpSysInfo*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Mci](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 

