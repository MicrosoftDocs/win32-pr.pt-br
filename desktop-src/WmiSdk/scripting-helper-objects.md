---
description: O WMI tem vários objetos auxiliares de script que fornecem as conversões exigidas pelos scripts.
ms.assetid: 832660b7-2992-4d1f-af16-7b8f0477b187
ms.tgt_platform: multiple
title: Objetos auxiliares de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 028079e49a2007d99b81f7832c4bce3cb016701d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789398"
---
# <a name="scripting-helper-objects"></a>Objetos auxiliares de script

O WMI tem vários objetos auxiliares de script que fornecem as conversões exigidas pelos scripts.

Os objetos auxiliares de script WMI incluem:

-   [**SWbemDateTime**](swbemdatetime.md)
-   [**SWbemObjectPath**](swbemobjectpath.md)
-   [**\_SecurityDescriptorHelper Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)

Os objetos auxiliares dividem as estruturas de dados compostos para que um script não seja necessário para analisar a estrutura para obter qualquer uma das partes. Por exemplo, a estrutura **DateTime de WMI** não pode ser exibida diretamente e é diferente de outras estruturas de dados DateTime do Windows, como a **\_ Data VT**.

## <a name="swbemdatetime"></a>SWbemDateTime

O objeto [**SWbemDateTime**](swbemdatetime.md) fornece propriedades que analisam o dia, o mês, o ano, a hora do dia e assim por diante. Ele também fornece métodos de conversão para converter o data e hora de Instrumentação de Gerenciamento do Windows (WMI) de e para os formatos de **\_ Data** e [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) do VT. Para configurações de segurança do Internet Explorer (IE), o objeto **SWbemDateTime** é o único objeto de script WMI que é marcado como seguro para inicialização e seguro para scripts. Para obter mais informações e exemplos de conversões de data e hora, consulte [datas e horas](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx) e o artigo sobre o TechNet ScriptCenter [é sobre o tempo (Ah, e também sobre datas)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).

## <a name="swbemobjectpath"></a>SWbemObjectPath

As propriedades de [**SWbemObjectPath**](swbemobjectpath.md) fornecem o caminho absoluto de um objeto, mas também dividem as partes do caminho do WMI, como servidor, namespace, classe ou caminho relativo. O objeto permite que você defina a segurança do caminho, obtenha os valores de chave dos objetos que representam o caminho, determine se um objeto é singleton e assim por diante. Para obter mais informações sobre como trabalhar com caminhos de objeto WMI, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).

## <a name="win32_securitydescriptorhelper"></a>\_SecurityDescriptorHelper Win32

A classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) converte o descritor de segurança de um objeto protegível de um formato para outro.

Muitos objetos, como impressoras, namespaces WMI, chaves do registro ou aplicativos DCOM, têm descritores de segurança que controlam o acesso ao objeto. Você pode usar o WMI para descobrir ou alterar quem tem acesso a esses objetos ao obter ou definir o descritor de segurança associado ao objeto.

No entanto, métodos diferentes podem obter descritores de segurança em uma matriz de bytes binários, no formato SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-string-format) ) ou como uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor). A forma da matriz de bytes binários de um descritor de segurança não deve ser manipulada, exceto pelos métodos do C++ projetados para [operações de descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-operations). Os descritores em SDDL estão em cadeias de caracteres, mas ainda são inconvenientes de manipular. O formato mais fácil de manipular é o **Win32 \_ SecurityDescriptor**, pois ele contém objetos incorporados para Trustee, Ace e Sid. Para obter mais informações sobre a estrutura de descritores de segurança no WMI, consulte [objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md). Para obter mais informações sobre como fazer conversões, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
