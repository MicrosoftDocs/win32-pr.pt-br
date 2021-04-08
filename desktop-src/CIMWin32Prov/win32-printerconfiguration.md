---
description: A \_ classe WMI PrinterConfiguration do Win32 representa a configuração de um dispositivo de impressora. Isso inclui recursos como resolução, cor, fontes e orientação.
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Classe Win32_PrinterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1927144484dbf427358735fc9d8ed66da56f3d8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920490"
---
# <a name="win32_printerconfiguration-class"></a>\_Classe Win32 PrinterConfiguration

A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterConfiguration do Win32** representa a configuração de um dispositivo de impressora. Isso inclui recursos como resolução, cor, fontes e orientação.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a>Membros

A classe **Win32 \_ PrinterConfiguration** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Win32 \_ PrinterConfiguration** tem essas propriedades.

<dl> <dt>

**BitsPerPel**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Número de bits usados para representar a cor nessa configuração (os bits por pixel). Esta propriedade está obsoleta. Em vez disso, use as propriedades nas classes [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) para determinar como a cor é representada.

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**Agrupar**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se **for true**, as páginas que são impressas devem ser agrupadas. Para se agrupar é imprimir o documento inteiro antes de imprimir a próxima cópia, em vez de imprimir cada página do documento o número necessário de vezes.

Essa propriedade é ignorada, a menos que o driver de impressora indique suporte para Agrupamento.

</dd> <dt>

**Cor**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cor do documento. Algumas impressoras coloridas têm a capacidade de imprimir usando preto em vez de uma combinação de ciano, magenta e amarelo (CMY). Isso geralmente cria texto mais escuro e mais nítido para documentos. Essa opção só é útil para impressoras coloridas que dão suporte à impressão em preto real.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Monocromático (preto verdadeiro)

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Cor

</dd> </dl>

</dd> <dt>

**Cópias**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de cópias a serem impressas. O driver de impressora deve dar suporte à impressão de cópias de várias páginas.

Exemplo: 2

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descrição textual do objeto atual.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**DeviceName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Nome amigável da impressora. Esse nome é exclusivo para o tipo de impressora e pode ser truncado devido às limitações da cadeia de caracteres da qual ela é derivada.

Exemplo: "PCL/HP LaserJet"

</dd> <dt>

**DisplayFlags**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o dispositivo de vídeo é colorido ou monocromático e se o tipo de verificação é não entrelaçado ou entrelaçado. Esta propriedade está obsoleta. Em vez disso, use Propriedades de exibição, como a propriedade **DisplayType** da classe **Win32 \_ DesktopMonitor** .

</dd> <dt>

**DisplayFrequency**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Exibe a taxa de atualização vertical. A taxa de atualização para um monitor é o número de vezes que a tela é redesenhada por segundo (frequência). Esta propriedade está obsoleta. Em vez disso, use as propriedades na classe [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)ou [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) .

</dd> <dt>

**Pontilhado**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de pontilhamento da impressora. Essa propriedade pode assumir valores predefinidos de 1 a 5 ou valores definidos pelo driver de 6 a 256. O pontilhamento de arte de linha é um método especial de pontilhamento que produz bordas bem definidas entre as escalas preta, branca e cinza. Ele não é adequado para imagens que incluem graduações contínuas em intensidade e matiz, como fotografias digitalizadas.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Sem pontilhamento

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Pincel grosso

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**Beta**


</dt> <dd>

Pincel fino

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**quatro**


</dt> <dd>

Arte de linhas

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**05**


</dt> <dd>

Escala de cinza

</dd> </dl>

</dd> <dt>

**DriverVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de versão do driver de impressora baseado no Windows. Os números de versão são criados e mantidos pelo fabricante do driver.

</dd> <dt>

**Duplex**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se for **true**, a impressão será feita em ambos os lados. Se for **false**, a impressão será feita em apenas um lado da mídia.

</dd> <dt>

**Tipo de formulário**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Não há suporte.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (pontos por polegada)
</dt> </dl>

Resolução de impressão em pontos por polegada ao longo do eixo x (largura) do trabalho de impressão (semelhante à propriedade **XResolution** obsoleta). Esse valor só é definido quando a propriedade **PrintQuality** dessa classe é positiva.

</dd> <dt>

**ICMIntent**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Valor específico de um dos três métodos de correspondência de cor possíveis (chamados de tentativas) que devem ser usados por padrão. Os aplicativos ICM estabelecem tentativas usando as funções ICM. Essa propriedade pode assumir valores predefinidos de 1 a 3 ou valores definidos pelo driver de 4 a 256. Aplicativos não ICM podem usar esse valor para determinar como a impressora trata os trabalhos de impressão colorida.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Saturação

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Contraste

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**Beta**


</dt> <dd>

Cor exata

</dd> </dl>

</dd> <dt>

**ICMMethod**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Como o ICM é manipulado. Para um aplicativo não ICM, essa propriedade determina se o ICM está habilitado ou desabilitado. Para aplicativos ICM, o sistema examina essa propriedade para determinar qual parte do sistema de computador trata do suporte a ICM.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Desabilitado

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Windows

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**Beta**


</dt> <dd>

Driver de dispositivo

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**quatro**


</dt> <dd>

Dispositivo

</dd> </dl>

</dd> <dt>

**LogPixels**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Número de pixels por polegada lógica. Essa propriedade obsoleta é válida somente com dispositivos que funcionam com pixels, o que exclui dispositivos como impressoras. Não há nenhum valor de substituição que se aplica a impressoras.

</dd> <dt>

**MediaType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tipo de mídia na qual a impressora é impressa. A propriedade pode ser definida como um valor predefinido ou um valor definido pelo driver maior ou igual a 256.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Standard

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Transparência

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**Beta**


</dt> <dd>

Acetinado

</dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](../wmisdk/standard-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome da impressora à qual esta configuração está associada. Esse valor corresponde à propriedade **Name** da instância de [**\_ impressora Win32**](win32-printer.md) associada.

</dd> <dt>

**Direção**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Orientação de impressão do papel.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Retrato

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Paisagem

</dd> </dl>

</dd> <dt>

**PaperLength**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (décimos de milímetro)
</dt> </dl>

Comprimento do papel. Para determinar o tamanho do papel em polegadas, divida esse valor por 254.

Exemplo: 2794

</dd> <dt>

**Papel**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Tamanho do papel. Os tamanhos possíveis são encontrados na propriedade **PaperSizesSupported** da classe de [**\_ impressora Win32**](win32-printer.md) associada.

Exemplo: "A4 ou letra".

</dd> <dt>

**PaperWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (décimos de milímetro)
</dt> </dl>

Largura do papel. Para determinar o tamanho do papel em polegadas, divida esse valor por 254.

Exemplo: 2159

</dd> <dt>

**PelsHeight**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Não há suporte a esta propriedade.

</dd> <dt>

**PelsWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Não há suporte a esta propriedade.

</dd> <dt>

**PrintQuality**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um dos quatro níveis de qualidade do trabalho de impressão. Se um valor positivo for especificado, a qualidade será medida em pontos por polegada.

<dt>

<span id="-1"></span>

<span id="-1"></span>**-1**


</dt> <dd>

Rascunho

</dd> <dt>

<span id="-2"></span>

<span id="-2"></span>**-2**


</dt> <dd>

Baixo

</dd> <dt>

<span id="-3"></span>

<span id="-3"></span>**-3**


</dt> <dd>

Médio

</dd> <dt>

<span id="-4"></span>

<span id="-4"></span>**-4**


</dt> <dd>

Alto

</dd> </dl>

</dd> <dt>

**Escala**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (porcentagem)
</dt> </dl>

Fator pelo qual a saída impressa deve ser dimensionada. Por exemplo, uma escala de 75 reduz a saída de impressão para 3/4 sua altura e largura originais.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador pelo qual o objeto atual é conhecido.

Essa propriedade é herdada [**da \_ configuração de CIM**](cim-setting.md).

</dd> <dt>

**SpecificationVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Número de versão dos dados de inicialização para o dispositivo associado à impressora baseada no Windows.

</dd> <dt>

**TTOption**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica como as fontes TrueType devem ser impressas.

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)


</dt> <dd>

Imprime fontes TrueType como elementos gráficos. Essa é a ação padrão para impressoras de matriz de pontos.

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Baixar** (2)


</dt> <dd>

Baixa fontes TrueType como fontes de disco. Essa é a ação padrão para impressoras que usam a PCL (linguagem de controle de impressora).

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Substituir** (3)


</dt> <dd>

Substitui as fontes de dispositivo por fontes TrueType. Essa é a ação padrão para impressoras PostScript.

</dd> </dl>

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) (pontos por polegada)
</dt> </dl>

Resolução de impressão ao longo do eixo y (altura) do trabalho de impressão (semelhante à propriedade **YResolution** obsoleta). Esse valor só é definido quando a propriedade **PrintQuality** dessa classe é positiva.

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Esta propriedade está obsoleta. Em vez disso, use a propriedade **HorizontalResolution** .

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **preteridos**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Esta propriedade está obsoleta. Em vez disso, use a propriedade **VerticalResolution** .

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ PrinterConfiguration** é derivada da [**\_ configuração de CIM**](cim-setting.md).

**Visão geral**

Antes de poder determinar como melhor distribuir e usar seus recursos de impressão, você deve ter um conhecimento detalhado desses recursos. Por exemplo, o departamento A pode ter apenas três impressoras comparadas com cinco impressoras no departamento B. No entanto, se as impressoras no departamento A podem imprimir 20 páginas por minuto e as impressoras no departamento B puderem imprimir apenas 5 páginas por minuto, os usuários no departamento A terão mais capacidade de impressão. Sem conhecer os recursos detalhados dessas impressoras, você pode concluir erroneamente que o departamento A é um pouco da capacidade de impressão e, portanto, comprar impressoras adicionais que acabam ficando sem uso.

O WMI inclui duas classes, a [**\_ impressora Win32**](win32-printer.md) e o **Win32 \_ PrinterConfiguration**, que podem ser usados para retornar informações detalhadas sobre todas as impressoras instaladas em um computador.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir recupera as informações da impressora.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                                |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>\_Impressora. mof do Win32</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração de CIM \_**](./cim-setting.md)
</dt> <dt>

[Classes de hardware do sistema de computador](computer-system-hardware-classes.md)
</dt> </dl>

 

 
