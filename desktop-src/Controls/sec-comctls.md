---
title: considerações de segurança sobre controles do Microsoft Windows
description: este tópico fornece informações sobre considerações de segurança relacionadas aos controles de Windows.
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45faa0f3d2f521038c056055329d70541625bac88c16e62c1581b55ae2a6c5bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696506"
---
# <a name="security-considerations-microsoft-windows-controls"></a>considerações de segurança: controles do Microsoft Windows

este tópico fornece informações sobre considerações de segurança relacionadas aos controles de Windows. As informações neste tópico não fornecem tudo o que você precisa saber sobre problemas de segurança — Use-o como ponto de partida e referência para essa área de tecnologia.

A interconectividade entre computadores é comum; a principal preocupação do desenvolvedor deve ser a segurança do aplicativo. as seções a seguir discutem alguns problemas potenciais de segurança a serem considerados ao programar Windows controles.

-   [Mensagens de controle terminadas em nulo](#null-terminated-control-messages)
-   [Uso de cadeia de caracteres](#string-use)
-   [Validação de entrada](#input-validation)
-   [Uso de senha](#password-use)
-   [Alertas de Segurança](#security-alerts)
-   [Tópicos relacionados](#related-topics)

## <a name="null-terminated-control-messages"></a>Mensagens de controle terminadas em nulo

Muitas das mensagens de controle e macros têm parâmetros de cadeia de caracteres. Geralmente, essas mensagens não validam as cadeias de caracteres de entrada, em particular, não verificam se há um encerramento `'\0'` . Quando você chama uma mensagem que usa uma cadeia de caracteres como parâmetro, especifique explicitamente que a cadeia de caracteres é terminada em nulo.

## <a name="string-use"></a>Uso de cadeia de caracteres

quando você programa Windows controles, é necessário manipular cadeias de caracteres. Quase todos os controles exigem que o texto seja inserido. Por exemplo, para preencher uma caixa de listagem, você deve carregar cadeias de caracteres no controle. Como usar cadeias de caracteres incorretamente geralmente causa estouros de buffer, tome precauções para evitar esse risco de segurança.

Para obter mais informações sobre estouros de buffer, consulte *escrevendo código seguro* por Michael Howard e David LeBlanc, Microsoft Press, 2002 e práticas [recomendadas para as APIs de segurança](/windows/desktop/SecBP/best-practices-for-the-security-apis).

## <a name="input-validation"></a>Validação da entrada

As mensagens de controle a seguir podem apresentar problemas de segurança.

-   [**\_GETLBTEXT CB**](cb-getlbtext.md)
-   [**\_GETISEARCHSTRING LVM**](lvm-getisearchstring.md)
-   [**SB \_ GETtext**](sb-gettext.md)
-   [**SB \_ GETTIPTEXT**](sb-gettiptext.md)
-   [**TB de \_ GETBUTTONTEXT**](tb-getbuttontext.md)
-   [**TTM \_ GETtext**](ttm-gettext.md)
-   [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md)

Se o texto for alterado entre a chamada para obter o comprimento do texto e a hora em que o texto for exibido ou usado, poderá ocorrer uma saturação do buffer. Para evitar isso, você deve validar a cadeia de caracteres antes de usá-la. Além disso, as mensagens que recuperam texto, [**CB \_ GETLBTEXT**](cb-getlbtext.md), [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)e [**TTM \_ gettext**](ttm-gettext.md), não têm nenhum parâmetro de tamanho de buffer que apresente o potencial para uma saturação de buffer.

Ao usar [**CB \_ GETLBTEXT**](cb-getlbtext.md) ou [**SB \_ gettext**](sb-gettext.md), você deve primeiro chamar [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) ou [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obter o tamanho do buffer. Algumas dessas mensagens, [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md), [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)e [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md), podem ser chamadas com um valor de parâmetro **nulo** para obter o comprimento da cadeia de caracteres antes de invocar a mensagem para recuperar a cadeia de caracteres.

Uma mensagem que você deve prestar atenção especial é a mensagem da barra de status [**SB \_ GETTIPTEXT**](sb-gettiptext.md) . Essa mensagem não fornece nenhuma maneira de consultar o comprimento da cadeia de caracteres que será recuperada.

## <a name="password-use"></a>Uso de senha

Se você usar controles de edição protegidos por senha (estilo de [**\_ senha es**](edit-control-styles.md) ), o buffer que contém o texto recuperado deverá ser definido como zero assim que possível para evitar a exposição da senha do usuário na memória.

## <a name="security-alerts"></a>Alertas de segurança

A tabela a seguir lista os recursos que, se usados incorretamente, podem comprometer a segurança de seus aplicativos. As mensagens listadas aqui não fornecem um parâmetro que especifica o tamanho do buffer.



| Recurso                                               | Atenuação                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | Verifique se o buffer usado pela função pode ser gravado e se está terminando em nulo.                                                                     |
| [**\_GETLBTEXT CB**](cb-getlbtext.md)                 | Chame [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) para obter o tamanho do buffer e, em seguida, chame [**CB \_ GETLBTEXT**](cb-getlbtext.md) para recuperar a cadeia de caracteres. |
| [**\_GETISEARCHSTRING LVM**](lvm-getisearchstring.md) | Chame a mensagem com um valor de parâmetro **nulo** para obter o tamanho do buffer e, em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres.             |
| [**SB \_ GETtext**](sb-gettext.md)                     | Chame [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) para obter o tamanho do buffer e, em seguida, chame [**SB \_ gettext**](sb-gettext.md) para recuperar a cadeia de caracteres.   |
| [**TB de \_ GETBUTTONTEXT**](tb-getbuttontext.md)         | Chame a mensagem com um valor de parâmetro **nulo** para obter o tamanho do buffer e, em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres.             |
| [**TTM \_ GETtext**](ttm-gettext.md)                   | Essa mensagem não fornece uma maneira de saber ou especificar o tamanho do buffer.                                                                  |
| [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md) | Chame a mensagem passando um valor de parâmetro **nulo** para obter o tamanho do buffer e, em seguida, chame a mensagem uma segunda vez para recuperar a cadeia de caracteres.       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Outros recursos**
</dt> <dt>

[Segurança da Microsoft](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[Segurança](/windows/desktop/security)
</dt> <dt>

[Recursos de segurança do TechNet](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[Práticas recomendadas para as APIs de segurança](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 