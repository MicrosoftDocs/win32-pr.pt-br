---
description: Você pode acessar todas as datas e horários de modelo CIM (CIM) no WMI usando um dos dois formatos de comprimento fixo específicos para WMI e CIM. No script, use o objeto SWbemDateTime para convertê-los em datas e horários regulares.
ms.assetid: 15126802-82f9-4ab4-98d8-0a15184302e9
ms.tgt_platform: multiple
title: CIM_DATETIME
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee4356050ee340cbf9d1b066f012d32c7185dd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765017"
---
# <a name="cim_datetime"></a>\_data e hora CIM

Você pode acessar todas as datas e horários de [*modelo CIM (CIM)*](gloss-c.md) no WMI usando um dos dois formatos de comprimento fixo específicos para WMI e CIM. No script, use o objeto [**SWbemDateTime**](swbemdatetime.md) para convertê-los em datas e horários regulares.

As seções a seguir descrevem como usar os formatos de data e hora do WMI.

## <a name="format"></a>Formatar

A tabela a seguir lista os dois formatos de data e hora usados pelo WMI.



| Formatar                                                                                                 | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [HORÁRIO](datetime.md)<br/> *AAAAMMDDHHMMSS. mmmmmmsUUU*<br/>                             | Formato no qual os valores de [**data e hora**](datetime.md) do CIM são armazenados. Esse formato é independente de localidade para que você possa escrever um script que seja executado em qualquer computador. Você deve usar esse formato para definir uma data e hora em [*formato MOF (MOF)*](gloss-m.md)ou ao gravar em uma instância do usando a [API com para WMI](com-api-for-wmi.md) ou a [API de script para WMI](scripting-api-for-wmi.md). Para obter mais informações, consulte [modificando uma propriedade de instância](modifying-an-instance-property.md). |
| Formato válido somente em consultas linguagem WQL (WQL).<br/> *aaaa-mm-dd HH: MM: SS: Mmm*<br/> | Esse formato pode ser usado em scripts que usam os métodos [**SWbemDateTime**](swbemdatetime.md) . Para obter mais informações, consulte [consultando o WMI](querying-wmi.md) ou [consultando com WQL](querying-with-wql.md). Esse formato não é independente da localidade. A ordem do ano, mês e dia depende da configuração de formato regional e de idioma da sessão do usuário. Por exemplo, embora o padrão para Estados Unidos inglês seja "mm-dd-aaaa hh: mm: SS: mmm", o formato para a maioria dos outros países ou regiões é "aaaa-mm-dd hh: mm: SS: mmm".       |



 

A tabela a seguir lista os campos nos formatos.



| Campo    | Descrição                                                                                                                                                                                                                                     |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *aaaa*   | Ano de quatro dígitos (0000 a 9999). Sua implementação pode restringir o intervalo com suporte. Por exemplo, uma implementação pode dar suporte apenas aos anos de 1980 a 2099.                                                                         |
| *mm*     | Mês de dois dígitos (01 a 12).                                                                                                                                                                                                                |
| *dd*     | Dia de dois dígitos do mês (01 a 31). Esse valor deve ser apropriado para o mês. Por exemplo, 31 de fevereiro não é válido. No entanto, sua implementação não precisa verificar se há dados válidos.                                            |
| *HH*     | A hora de dois dígitos do dia usando o relógio de 24 horas (00 a 23).                                                                                                                                                                              |
| *MM*     | Minuto de dois dígitos na hora (00 a 59).                                                                                                                                                                                                   |
| *II*     | Número de segundos de dois dígitos no minuto (00 a 59).                                                                                                                                                                                      |
| *mmmmmm* | Número de seis dígitos de microssegundos no segundo (000000 a 999999). Sua implementação não precisa dar suporte à avaliação usando esse campo. No entanto, esse campo sempre deve estar presente para preservar a natureza de comprimento fixo da cadeia de caracteres. |
| *mmm*    | Número de milissegundos de três dígitos no minuto (000 a 999).                                                                                                                                                                             |
| *s*      | Sinal de mais (+) ou subtração (-) para indicar um deslocamento positivo ou negativo do UTC (tempo Universal Coordenado).                                                                                                                               |
| *UUU*    | Deslocamento de três dígitos que indica o número de minutos que o fuso horário de origem desvia do UTC. Para o WMI, ele é incentivado, mas não é necessário, para converter horas em GMT (um deslocamento UTC de zero).                                              |



 

Você deve inserir todos os campos com o comprimento indicado, usando zeros à esquerda, conforme apropriado para o tipo. No entanto, use asteriscos para indicar campos não utilizados ou como um valor de curinga. Você pode usar um asterisco ( \* ) em todos os lugares, exceto a cláusula **Where** de uma consulta. Por exemplo, uma data e hora com um ano não especificado podem ocorrer em qualquer ano. Se você quiser deixar um campo não especificado, deverá substituir o campo inteiro por asteriscos.

Os exemplos a seguir descrevem usos válidos e inválidos de asteriscos:

-   19980416 \* \* \* \* \* \* .000000 + \* \* \* (legal)
-   1998-04-16 \* \* \* \* \* \* : \* \* \* (inválido)
-   199 \* 0416 \* \* \* \* \* \* .000000 + \* \* \* (inválido)
-   199 \* -04-16 \* \* \* \* \* \* : \* \* \* (inválido)

Se um DateTime for usado para representar um ponto específico no tempo, todos os seus campos deverão incluir dados. Se for usado para representar um intervalo de tempo, somente os campos necessários para transmitir a duração deverão incluir dados.

O exemplo a seguir descreve "1º de abril": uma data relativa a algum ano não especificado, mas ainda um ponto definido se o nível de detalhe de medida for um dia.

-   \*\*\*\*0401 \* \* \* \* \* \* . 000000 +\*\*\*
-   \*\*\*\*-04-01 \* \* \* \* \* \* : \* \* \* (inválido)

## <a name="setting-utc-offset-and-gmt"></a>Definindo o deslocamento UTC e o GMT

Os exemplos a seguir descrevem como você pode definir uma hora sem fuso horário colocando asteriscos no campo UUU após o sinal de adição ou subtração:

-   19980401135809.000000 +\*\*\*
-   19980401135809, 0-\*\*\*
-   1998-04-01 13:58:09: \* \* \* (inválido)

Um aplicativo interpreta uma referência de data e hora sem zona para um Chronometer local e abstrato no sistema operacional em execução. Por exemplo, computadores portáteis podem ter relógios internos cujas configurações podem ou não corresponder ao fuso horário geográfico. Você pode interpretar o tempo não-zoneado substituindo o fuso horário da fonte de tempo abstrata atual em vez do fuso horário local.

Você deve dar uma consideração especial ao significado do deslocamento UTC com datas e horas em consultas. Em geral, as comparações de equivalência, maior que ou menor que funcionam entre duas datas e horas se as datas e horas usam o mesmo deslocamento UTC. Ao lidar com datas e horas que ocorrem com deslocamentos de fuso horário diferentes, primeiro você deve converter as datas e horas em GMT.

As consultas que envolvem datas e horas relativas com asteriscos em um ou mais subcampos só são significativas para o WMI quando comparadas à equivalência. Além disso, o WMI não permite o uso de asteriscos como curingas. Em vez disso, o WMI compara datas e horas relativas em uma base de caractere por caractere.

Os exemplos a seguir descrevem duas datas em que uma consulta WMI não considera igual:

-   19980401135809.000000 +\*\*\*
-   19980401135809.000000 + 000

## <a name="converting-to-filetime-or-vt_date-format"></a>Convertendo para formato de data do FILETIME ou VT \_

O formato de [**data e hora**](datetime.md) CIM é usado somente dentro do WMI. Você pode converter de e para o formato do WMI e o formato de data do FILETIME ou VT \_ chamando os métodos do objeto de script [**SWbemDateTime**](swbemdatetime.md) . Uma estrutura de **data e hora** [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) é um valor de 64 bits que os sistemas operacionais Windows de 32 bits usam. \_O formato de data VT é um valor DateTime de variante de automação usado por Visual Basic e ActiveX. A tabela a seguir lista os métodos de conversão.



| Método                                                         | Descrição                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime. GetFileTime**](swbemdatetime-getfiletime.md) | Obtém um valor [**DateTime**](datetime.md) no formato [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .                |
| [**SWbemDateTime. GetVarDate**](swbemdatetime-getvardate.md)   | Obtém um valor [**DateTime**](datetime.md) no \_ formato de data VT.                                         |
| [**SWbemDateTime. SetFileTime**](swbemdatetime-setvardate.md)  | Define uma propriedade [**DateTime**](datetime.md) usando uma data [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) como entrada. |
| [**SWbemDateTime. SetVarDate**](swbemdatetime-setvardate.md)   | Define uma propriedade [**DateTime**](datetime.md) usando uma data de \_ Data VT como entrada.                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato de data e hora](date-and-time-format.md)
</dt> <dt>

[Sobre o WMI](about-wmi.md)
</dt> <dt>

[Tarefas do WMI: datas e horas](wmi-tasks--dates-and-times.md)
</dt> <dt>

[Formato do intervalo](interval-format.md)
</dt> <dt>

[**SWbemObject. put\_**](swbemobject-put-.md)
</dt> <dt>

[**SWbemServicesEx. put**](swbemservicesex-put.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)
</dt> <dt>

[**IWbemServices::P utClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)
</dt> </dl>

 

