---
description: Os serviços de certificados fornecem páginas de registro da Web que podem ser usadas para solicitar certificados.
ms.assetid: 1e198bc8-c712-4d0f-9e3a-35a295445acf
title: Personalizando páginas de registro na Web de serviços de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0132ce4e5e1fef588ffc429597717433dd1b780d2f7f35f9c886f1978b5b318a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767791"
---
# <a name="customizing-certificate-services-web-enrollment-pages"></a>Personalizando páginas de registro na Web de serviços de certificados

Os [*serviços de certificados*](../secgloss/c-gly.md) fornecem páginas de registro da Web que podem ser usadas para solicitar certificados. Um administrador pode personalizar alguns dos itens que podem ser exibidos nas páginas de registro da Web; no entanto, você deve estar familiarizado com as páginas de registro da Web e o script da Web antes de fazer qualquer alteração. Para obter mais informações sobre scripts da Web, consulte [scripts](/previous-versions/ms950396(v=msdn.10)).

Os valores padrão para os campos de nome distinto para organização, unidade organizacional, localidade, estado e país/região são os valores especificados para a [*autoridade de certificação*](../secgloss/c-gly.md) (CA) quando os serviços de certificados são instalados. Esses valores padrão aparecem nas páginas da Web e podem ser alterados pelo usuário durante o processo de registro de certificado. No entanto, se você quiser que outros valores padrão apareçam nas páginas da Web, poderá editar o arquivo Certdat. Inc (no caminho \\ *WindowsDirectory* \\ System32 \\ certsrv \\ ); especificamente, você pode atribuir valores personalizados às seguintes variáveis fornecidas para personalização.



| Variável            | Descrição                                                                                                                                                                                                                               |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sDefaultCompany     | Empresa padrão (aparece na [*solicitação de certificado*](../secgloss/c-gly.md) como o campo de organização [*X. 509*](../secgloss/x-gly.md) ). |
| sDefaultOrgUnit     | Departamento padrão (aparece na solicitação de certificado como o campo de unidade organizacional X. 509).                                                                                                                                           |
| sDefaultLocality    | Cidade padrão (aparece na solicitação de certificado como o campo de local X. 509).                                                                                                                                                            |
| sDefaultState       | Estado/província padrão (aparece na solicitação de certificado como o campo de estado X. 509).                                                                                                                                                     |
| sDefaultCountry     | País/região padrão (aparece na solicitação de certificado como o campo país/região X. 509).                                                                                                                                            |
| nPendingTimeoutDays | Número de dias em que o usuário pode recuperar um certificado pendente depois que ele é solicitado.                                                                                                                                          |



 

Nenhuma outra variável deve ser alterada no arquivo Certdat. Inc.

O exemplo a seguir define a unidade organizacional padrão como "marketing".


```VB
sDefaultOrgUnit="Marketing"
```



Além disso, você pode editar o arquivo Certrqtp. Inc para adicionar, alterar ou remover [*modelos de certificado*](../secgloss/c-gly.md) ou tipos disponíveis para o usuário. Esses modelos e tipos, bem como informações relacionadas, estão contidos em uma matriz dimensionada chamada rgAvailReqTypes (*m*, 5).

essa matriz, como todas as matrizes do Visual Basic scripting Edition, é baseada em zero e, como resultado, a primeira dimensão da matriz, *m*, aloca memória para *m*+ 1 items. Portanto, se, ao personalizar as páginas da Web, você precisar modificar o número de itens na matriz rgAvailReqTypes, defina a dimensão *m* para uma menor do que o número total de itens necessários. Por exemplo, se você tiver sete modelos de certificado, altere a declaração de rgAvailReqTypes, conforme mostrado no exemplo a seguir.


```VB
Dim rgAvailReqTypes(6,5)
```



A segunda dimensão da matriz, que sempre tem o valor cinco, aloca os seis campos que compõem cada item. Esses seis campos representam o modelo ou tipo de certificado, o nome de exibição associado a este modelo ou tipo, e se o modelo requer S/MIME ( [*extensões de email da Internet) seguras/multipropósitos*](../secgloss/s-gly.md) .

Para facilitar a compreensão de quais desses campos está sendo acessado, a Certrqtp. Inc também fornece as seguintes constantes que você pode usar ao definir valores de campo.



| Constante                              | Descrição                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **OID do campo \_**                        | (Aplica-se a CAs autônomas) Indexar para o primeiro campo do item; representa um OID ( [*identificador de objeto*](../secgloss/o-gly.md) ) para um tipo de certificado.<br/>                                                                                                           |
| **modelo de campo \_**                   | (Aplica-se a CAs corporativas) Indexar para o primeiro campo do item; representa um modelo de certificado.<br/>                                                                                                                                                                                                                           |
| **\_FriendlyName do campo**               | Índice para o segundo campo do item; representa o nome de exibição (que o usuário verá ao registrar) do item no primeiro campo.                                                                                                                                                                                               |
| **CSPLIST de campo \_**                    | Índice para o terceiro campo do item. Uma lista de nomes de [*provedores de serviços de criptografia*](../secgloss/c-gly.md) permitidos pelo modelo. Cada nome na lista é separado por um ponto de interrogação (?).                                                    |
| **CSPLIST2 de campo \_**                   | Índice para o quarto campo do item. Uma lista secundária de nomes de [*provedores de serviços de criptografia*](../secgloss/c-gly.md) permitidos pelo modelo. Cada nome na lista é separado por um ponto de interrogação (?). Essa lista fornece um padrão diferente. |
| **CAMPO \_ EXportável**                 | Índice para o quinto campo do item. Indica se o modelo especifica que a chave deve ser exportável. Se esse campo contiver "true", a chave será exportável. Se esse campo contiver "false", a chave não será exportável.                                                                                                        |
| **o campo \_ precisa de \_ \_ recursos SMIME** | Não há suporte para essa constante.                                                                                                                                                                                                                                                                                                      |



 

Por exemplo, as expressões a seguir atribuem o OID de 1.3.6.1.5.5.7.3.2 ao primeiro campo do primeiro item e atribuimos "certificado do navegador da Web" ao segundo campo do primeiro item (o valor de matriz de zero indexa o primeiro item).


```VB
rgAvailReqTypes(0, FIELD_OID) = "1.3.6.1.5.5.7.3.2"
rgAvailReqTypes(0, FIELD_FRIENDLYNAME) = "Web Browser Certificate"
```



O resultado dessas atribuições é que o usuário verá o texto **certificado do navegador da Web** ao registrar e, se o usuário selecionar o **certificado do navegador da Web**, a [*solicitação de certificado*](../secgloss/c-gly.md) conterá o OID 1.3.6.1.5.5.7.3.2.

O arquivo Certrqtp. Inc também contém constantes que são usadas para os nomes de exibição dos modelos de certificado ou tipos. O exemplo a seguir mostra o formato.


```VB
' Strings for localization.
Const L_WebBrowserCert_Text="Web Browser Certificate"
Const L_EmailProtectionCert_Text="E-Mail Protection Certificate"
Const L_UserTemplateCert_Text="User Certificate"
```



Essas constantes são definidas em um bloco no arquivo Certrqtp. Inc, e esse agrupamento torna mais fácil atribuir a cada um valor personalizado. Isso é particularmente útil quando você localiza os nomes de exibição para versões internacionais das páginas da Web.

Por fim, o arquivo Certrqtp. Inc contém uma variável que representa o número de modelos de certificado ou tipos na matriz rgAvailReqTypes. Ao contrário da dimensão *m* da matriz, defina o valor da variável nAvailReqTypes como o número real de modelos de certificado ou tipos que sua instalação usará; Esse valor não deve ser maior que *m*+ 1. Embora declarado próximo à parte superior do arquivo Certrqtp. Inc, o nAvailReqTypes recebe um valor depois que a matriz rgAvailReqTypes é populada, facilitando a visualização de quantos elementos são realmente usados pela matriz. O valor nAvailReqTypes é usado em uma iteração em outro lugar nas páginas de registro da Web, portanto, é importante que essa variável reflita com precisão o número de modelos de certificado ou tipos que você deseja que sejam visíveis para o usuário.

Observe que meramente adicionar [*modelos de certificado*](../secgloss/c-gly.md) e tipos ao arquivo Certrqtp. Inc não garante que o usuário poderá obter um certificado com essas características; a AC deve estar autorizada a emitir um certificado para o modelo ou tipo de certificado especificado.

As instalações podem criar seus próprios aplicativos ou páginas da Web para solicitar e receber um certificado. Os objetos [**ICEnroll4**](/windows/desktop/api/Xenroll/nn-xenroll-icenroll4) e [**ICertRequest2**](/windows/desktop/api/Certcli/nn-certcli-icertrequest2) permitem que programadores ou criadores de scripts criem aplicativos de [*solicitação de certificado*](../secgloss/c-gly.md) .

Para solicitar um certificado a ser emitido em um [*cartão inteligente*](../secgloss/s-gly.md), você pode usar o controle de registro de cartão inteligente. Para obter detalhes e código de exemplo, consulte [**ISCrdEnr**](iscrdenr.md).

 

 
