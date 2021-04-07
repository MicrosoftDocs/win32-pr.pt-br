---
title: MCI_SYSINFO comando (mmsystem. h)
description: O comando do sysinfo do MCI \_ recupera informações sobre dispositivos MCI.
ms.assetid: 605efd25-8849-42aa-99fd-b36b6fd2c7b7
keywords:
- Multimídia do Windows de comando MCI_SYSINFO
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
ms.openlocfilehash: e722625449893771726a83738c3b0d7bc8bc523c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918558"
---
# <a name="mci_sysinfo-command"></a>Comando do sysinfo do MCI \_

O comando do sysinfo do MCI \_ recupera informações sobre dispositivos MCI. O MCI dá suporte a esse comando diretamente, em vez de passá-lo para o dispositivo. Qualquer aplicativo MCI pode usar esse comando. As informações de cadeia de caracteres são retornadas no buffer fornecido pelo aplicativo apontado pelo membro **lpstrReturn** da estrutura identificada por *lpSysInfo*. Informações numéricas são retornadas como um valor **DWORD** colocado no buffer fornecido pelo aplicativo. O membro **dwRetSize** especifica o comprimento do buffer.

Para enviar esse comando, chame a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) com os parâmetros a seguir.


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

<span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*
</dt> <dd>

Um ou mais dos seguintes sinalizadores padrão e específicos de comando:

</dd> <dt>

<span id="MCI_SYSINFO_INSTALLNAME"></span><span id="mci_sysinfo_installname"></span>instalação do do sysinfo do MCI \_ \_
</dt> <dd>

Obtém o nome (listado no registro ou o arquivo de SYSTEM.INI) usado para instalar o dispositivo.

</dd> <dt>

<span id="MCI_SYSINFO_NAME"></span><span id="mci_sysinfo_name"></span>\_nome do sysinfo do MCI \_
</dt> <dd>

Obtém um nome de dispositivo correspondente ao número do dispositivo especificado no membro **dwNumber** da estrutura identificada por **lpSysInfo**. Se o sinalizador de abertura do sysinfo do MCI \_ \_ estiver definido, o MCI retornará os nomes dos dispositivos abertos.

</dd> <dt>

<span id="MCI_SYSINFO_OPEN"></span><span id="mci_sysinfo_open"></span>\_Open sysinfo do MCI \_
</dt> <dd>

Obtém a quantidade ou o nome dos dispositivos abertos.

</dd> <dt>

<span id="MCI_SYSINFO_QUANTITY"></span><span id="mci_sysinfo_quantity"></span>\_quantidade de sysinfo do MCI \_
</dt> <dd>

Obtém o número de dispositivos do tipo especificado que estão listados no registro ou na \[ \] seção MCI do arquivo de SYSTEM.INI. Se o sinalizador de abertura do sysinfo do MCI \_ \_ estiver definido, o número de dispositivos abertos será retornado.

</dd> <dt>

<span id="lpSysInfo"></span><span id="lpsysinfo"></span><span id="LPSYSINFO"></span>*lpSysInfo*
</dt> <dd>

Ponteiro para uma estrutura [**MCI de \_ \_ parâmetros do sysinfo**](mci-sysinfo-parms.md) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro de outra forma.

## <a name="remarks"></a>Comentários

O membro **wDeviceType** da estrutura identificada por *lpSysInfo* é usado para indicar o tipo de dispositivo da consulta. Se o parâmetro *wDeviceID* for definido como MCI \_ todos \_ os \_ IDs de dispositivo, ele substituirá o valor de **wDeviceType**. Para obter uma lista de tipos de dispositivo, consulte [tipos de dispositivo MCI](mci-device-types.md).

Valores de retorno de inteiros são valores **DWORD** retornados no buffer apontados pelo membro **lpstrReturn** da estrutura identificada por *lpSysInfo*.

Os valores de retorno de String são cadeias de caracteres terminadas em nulo retornadas no buffer apontado pelo membro **lpstrReturn** da estrutura identificada por *lpSysInfo*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Comandos MCI](mci-commands.md)
</dt> </dl>

 

