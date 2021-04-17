---
title: Classe SystemRestoreConfig
description: Fornece propriedades para controlar a frequência de criação de ponto de restauração agendada e a quantidade de espaço em disco consumida em cada unidade.
ms.assetid: ed09e03f-8cc1-4923-8f39-bbe7d9a19b44
keywords:
- Restauração do sistema de classe SystemRestoreConfig
- Restauração do sistema de classe SystemRestoreConfig, descrita
topic_type:
- apiref
api_name:
- SystemRestoreConfig
- SystemRestoreConfig.RPSessionInterval
- SystemRestoreConfig.RPGlobalInterval
- SystemRestoreConfig.RPLifeInterval
- SystemRestoreConfig.DiskPercent
api_location:
- Root\Default
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58ded8a17cc4800e1aa2917ba7750c6c69434916
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369709"
---
# <a name="systemrestoreconfig-class"></a>Classe SystemRestoreConfig

Fornece propriedades para controlar a frequência de criação de ponto de restauração agendada e a quantidade de espaço em disco consumida em cada unidade.

## <a name="syntax"></a>Sintaxe

``` syntax
class SystemRestoreConfig
{
  uint32 RPSessionInterval;
  uint32 RPGlobalInterval;
  uint32 RPLifeInterval;
  uint32 DiskPercent;
};
```

## <a name="members"></a>Membros

A classe **SystemRestoreConfig** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **SystemRestoreConfig** tem essas propriedades.

<dl> <dt>

**DiskPercent**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A quantidade máxima de espaço em disco em cada unidade que pode ser usada pela restauração do sistema. Esse valor é especificado como uma porcentagem do espaço total na unidade. O valor padrão é 12%.

**Windows Vista:** Recebe um valor da Serviço de Cópias de Sombra de Volume (VSS). Esta é a quantidade máxima de espaço em disco em cada unidade que pode ser usada pela restauração do sistema. O valor padrão é 15% do espaço total da unidade ou 30 por cento do espaço livre disponível, o que for menor.

</dd> <dt>

**RPGlobalInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O intervalo de tempo absoluto no qual os pontos de verificação do sistema agendados são criados, em segundos. O valor padrão é 86.400 (24 horas).

**Windows Vista:** Recebe um valor do Agendador de tarefas para restauração do sistema. Zero se a tarefa estiver desabilitada.

</dd> <dt>

**RPLifeInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O intervalo de tempo para o qual os pontos de restauração são preservados, em segundos. Quando um ponto de restauração se torna mais antigo que esse intervalo especificado, ele é excluído. O limite de idade padrão é de 90 dias.

**Windows Vista:** Recebe um valor de **UINTMAX**.

</dd> <dt>

**RPSessionInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O intervalo de tempo no qual os pontos de verificação do sistema agendados são criados durante a sessão, em segundos. O valor padrão é zero, indicando que o recurso está desativado.

**Windows Vista:** Receberá zero se a restauração do sistema estiver desabilitada.

</dd> </dl>

## <a name="examples"></a>Exemplos

Não há suporte para o código de exemplo a seguir. Use a ferramenta de linha de comando Vssadmin.exe para alterar o tamanho do espaço reservado da unidade.

**Windows XP:** Há suporte para este exemplo.


```VB
'The SystemRestoreConfig class provides properties for controlling the frequency of 
'scheduled restore point creation and the amount of disk space consumed on each drive.

Set Args = wscript.Arguments
Set regSR = GetObject("winmgmts:{impersonationLevel=impersonate}!root/default:SystemRestoreConfig='SR'")

If Args.Count() = 0 Then
    Wscript.Echo "Usage: RegSR [RP{Session|Global|Life}Interval[=value]] [DiskPercent[=value]]"
Else    
For i = 0 To Args.Count() - 1
    Myarg = Args.Item(i)
    Pos = InStr(Myarg, "=")
    If Pos <> 0 Then
        Myarray = Split(Myarg, "=", -1, 1)
        myoption = Myarray(0)
        value = Myarray(1)
    Else 
        myoption = Myarg
    End If    
    If myoption = "RPSessionInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPSessionInterval = " & regSR.RPSessionInterval
        Else    
            regSR.RPSessionInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPGlobalInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPGlobalInterval = " & regSR.RPGlobalInterval
        Else    
            regSR.RPGlobalInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "RPLifeInterval" Then
        If Pos = 0 Then
            Wscript.Echo "RPLifeInterval = " & regSR.RPLifeInterval
        Else    
            regSR.RPLifeInterval = value
            regSR.Put_
        End If
    ElseIf myoption = "DiskPercent" Then
        If Pos = 0 Then
            Wscript.Echo "DiskPercent = " & regSR.DiskPercent
        Else    
            regSR.DiskPercent = value
            regSR.Put_
        End If
    End If
Next
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                         |
| Namespace<br/>                | \\Padrão raiz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Sr. mof</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Pontos de restauração](restore-points.md)
</dt> <dt>

[Instrumentação de Gerenciamento do Windows](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

