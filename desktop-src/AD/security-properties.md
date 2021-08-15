---
title: Atributos de segurança do usuário
description: Além de nomear Propriedades para objetos de usuário, por exemplo, objectGUID, objectSID, CN, distinguishedName e assim por diante, há outras propriedades de segurança usadas para logon, acesso à rede e controle de acesso.
ms.assetid: eeb16938-4380-4622-804f-6b2ff19aa68d
ms.tgt_platform: multiple
keywords:
- Atributos de segurança, usando o AD
- AD atributos de segurança do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dfe23252002f2ffbbba3f8e8a8faf5a2d36ce348bdbd7503c0d99a816a81902
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024884"
---
# <a name="user-security-attributes"></a>Atributos de segurança do usuário

Além de nomear Propriedades para objetos de usuário, por exemplo, [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSid**](/windows/desktop/ADSchema/a-objectsid), [**CN**](/windows/desktop/ADSchema/a-cn), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname)e assim por diante, há outras propriedades de segurança usadas para logon, acesso à rede e controle de acesso. essas propriedades são usadas pelo sistema de segurança Windows 2000. Essas propriedades podem ser exibidas e gerenciadas pelo snap-in Active Directory usuário e computadores.

<dl> <dt>

<span id="accountExpires"></span><span id="accountexpires"></span><span id="ACCOUNTEXPIRES"></span>[**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)
</dt> <dd>

O atributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) especifica quando uma conta expira. Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601 (UTC). Um valor de **TIMEQ para \_ sempre** (definido em Lmaccess. h) indica que uma conta nunca expira.

</dd> <dt>

<span id="altSecurityIdentities"></span><span id="altsecurityidentities"></span><span id="ALTSECURITYIDENTITIES"></span>[**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities)
</dt> <dd>

O atributo [**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities) é um atributo com vários valores que contém mapeamentos para certificados X. 509 ou contas de usuário Kerberos externas para esse usuário para fins de autenticação. vários pacotes de segurança, incluindo o pacote de autenticação de chave pública e o Kerberos, usam esses dados para autenticar usuários quando eles apresentam a forma alternativa de identificação, como certificado, UNIX tíquete Kerberos e assim por diante. crie um token Windows 2000 com base na conta de usuário correspondente, de modo que eles possam acessar os recursos do sistema.

Para certificados X. 509, os valores devem ser os nomes do emissor e da entidade em certificados do 509v3, emitidos por uma autoridade de certificação pública externa, que é mapeada para a conta de usuário usada para encontrar uma conta para autenticação. O pacote SSL (Schannel) usa a seguinte sintaxe: X509: <somecertinfotype> somecertinfo. Por exemplo, o valor a seguir especifica o DN do emissor " \<I\> " com o DN "c = US, O = InternetCA, CN = APublicCertificateAuthority" e o DN do assunto " \<S\> " com o DN "c = US, o = Fabrikam, ou = Sales, CN = Jeff Smith".


```C++
X509:<I>C=US,O=InternetCA,CN=APublicCertificateAuthority<S>C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith
```



Lembre-se de que " \<S\> " ou " \<I> " e " \<S\> " têm suporte. \<I\>Não há suporte para apenas "". Os aplicativos não devem modificar os valores em " \<I\> " ou " \<S\> " porque a correspondência de DN parcial não tem suporte.

Para contas Kerberos externas, os valores devem ser o nome da conta Kerberos. O pacote Kerberos usa a seguinte sintaxe: "Kerberos: MITaccountname". Por exemplo, este é o valor de uma conta em Fabrikam.com:


```C++
Kerberos:Jeff.Smith@Fabrikam.com
```



</dd> <dt>

<span id="badPasswordTime"></span><span id="badpasswordtime"></span><span id="BADPASSWORDTIME"></span>[**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)
</dt> <dd>

Não replicado. O atributo [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime) especifica a última vez que o usuário tentou fazer logon na conta usando uma senha incorreta. Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601 (UTC). Esse atributo é mantido separadamente em cada controlador de domínio no domínio. Um valor de zero significa que a hora da última senha inadequada é desconhecida. Para obter um valor preciso para o último tempo de senha incorreto do usuário no domínio, cada controlador de domínio no domínio deve ser consultado e o maior valor deve ser usado.

</dd> <dt>

<span id="badPwdCount"></span><span id="badpwdcount"></span><span id="BADPWDCOUNT"></span>[**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)
</dt> <dd>

Não replicado. O atributo [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount) especifica o número de vezes que o usuário tentou fazer logon na conta usando uma senha incorreta. Esse atributo é mantido separadamente em cada controlador de domínio no domínio. Um valor de 0 indica que o valor é desconhecido. Para obter um valor preciso para as tentativas totais de senha incorreta do usuário no domínio, cada controlador de domínio no domínio deve ser consultado e a soma dos valores deve ser usada.

</dd> <dt>

<span id="codePage"></span><span id="codepage"></span><span id="CODEPAGE"></span>[**Código**](/windows/desktop/ADSchema/a-codepage)
</dt> <dd>

O atributo [**CodePage**](/windows/desktop/ADSchema/a-codepage) especifica a página de código para o idioma escolhido pelo usuário. esse valor não é usado pelo Windows 2000.

</dd> <dt>

<span id="countryCode"></span><span id="countrycode"></span><span id="COUNTRYCODE"></span>[**countryCode**](/windows/desktop/ADSchema/a-countrycode)
</dt> <dd>

O atributo [**CountryCode**](/windows/desktop/ADSchema/a-countrycode) especifica o código de país/região para o idioma do usuário. esse valor não é usado pelo Windows 2000.

</dd> <dt>

<span id="homeDirectory"></span><span id="homedirectory"></span><span id="HOMEDIRECTORY"></span>[**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)
</dt> <dd>

O atributo [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) especifica o caminho do diretório base para o usuário. A cadeia de caracteres pode ser nula.

Se [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) for definido e especificar uma letra de unidade, [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) deverá ser um caminho UNC. O caminho deve ser um caminho UNC de rede do diretório de compartilhamento do servidor de formulário \\ \\ \\ \\ . Esse valor pode ser uma cadeia de caracteres nula.

Se [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) não for definido, [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) deverá ser um caminho local, por exemplo, C: \\ mylocaldir.

</dd> <dt>

<span id="homeDrive"></span><span id="homedrive"></span><span id="HOMEDRIVE"></span>[**homeDrive**](/windows/desktop/ADSchema/a-homedrive)
</dt> <dd>

O atributo [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) especifica a letra da unidade para a qual mapear o caminho UNC especificado por **HomeDirectory**. A letra da unidade deve ser especificada no seguinte formato:


```C++
<drive letter>:
```



onde " \<drive letter\> " é a letra da unidade a ser mapeada. Por exemplo:


```C++
Z:
```



Se esse atributo não for definido, o [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) deverá ser um caminho local, por exemplo, C: \\ mylocaldir.

</dd> <dt>

<span id="lastLogoff"></span><span id="lastlogoff"></span><span id="LASTLOGOFF"></span>[**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)
</dt> <dd>

Não replicado. O atributo [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff) especifica quando o último logoff ocorreu. Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601 (UTC). A parte superior desse inteiro grande corresponde ao membro **dwHighDateTime** da estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e a parte inferior corresponde ao membro **dwLowDateTime** da estrutura **FILETIME** . Esse atributo é mantido separadamente em cada controlador de domínio no domínio. Um valor de zero significa que a hora do último logoff é desconhecida. Para obter um valor preciso para o último logoff do usuário no domínio, cada controlador de domínio no domínio deve ser consultado e o maior valor deve ser usado.

</dd> <dt>

<span id="lastLogon"></span><span id="lastlogon"></span><span id="LASTLOGON"></span>[**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)
</dt> <dd>

Não replicado. O atributo [**LastLogon**](/windows/desktop/ADSchema/a-lastlogon) especifica quando ocorreu o último logon. Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 a nanossegundos desde 1º de janeiro de 1601 (UTC). A parte superior desse inteiro grande corresponde ao membro **dwHighDateTime** da estrutura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) e a parte inferior corresponde ao membro **dwLowDateTime** da estrutura **FILETIME** . Esse atributo é mantido separadamente em cada controlador de domínio no domínio. Um valor de zero significa que a hora do último logon é desconhecida. Para obter um valor preciso para o último logon do usuário no domínio, cada controlador de domínio no domínio deve ser consultado e o maior valor deve ser usado.

</dd> <dt>

<span id="lmPwdHistory"></span><span id="lmpwdhistory"></span><span id="LMPWDHISTORY"></span>[**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory)
</dt> <dd>

O atributo [**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory) é o histórico de senha do usuário no formato unidirecional do LM (LAN Manager). o LM OWF é usado para compatibilidade com clientes do LAN Manager 2. x, Windows 95 e Windows 98. Esse atributo é usado somente pelo sistema operacional. Lembre-se de que você não pode derivar a senha de texto não criptografado da forma OWF da senha.

</dd> <dt>

<span id="logonCount"></span><span id="logoncount"></span><span id="LOGONCOUNT"></span>[**logonCount**](/windows/desktop/ADSchema/a-logoncount)
</dt> <dd>

Não replicado. O atributo [**logonCount**](/windows/desktop/ADSchema/a-logoncount) conta o número de vezes com êxito que o usuário tentou fazer logon nessa conta. Esse atributo é mantido em cada controlador de domínio no domínio. Um valor de 0 indica que o valor é desconhecido. Para obter um valor preciso para o número total de tentativas de logon bem-sucedidas do usuário no domínio, cada controlador de domínio no domínio deve ser consultado e a soma dos valores deve ser usada.

</dd> <dt>

<span id="mail"></span><span id="MAIL"></span>[**mescla**](/windows/desktop/ADSchema/a-mail)
</dt> <dd>

O atributo de [**email**](/windows/desktop/ADSchema/a-mail) é um atributo de valor único que contém o endereço SMTP para o usuário, por exemplo, " jeff@Fabrikam.com ".

</dd> <dt>

<span id="maxStorage"></span><span id="maxstorage"></span><span id="MAXSTORAGE"></span>[**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)
</dt> <dd>

O atributo [**maxStorage**](/windows/desktop/ADSchema/a-maxstorage) especifica a quantidade máxima de espaço na unidade de disco rígido que o usuário pode usar. Use o valor do **usuário \_ MAXSTORAGE \_ ilimitado** (definido no Lmaccess. h) para usar todo o espaço em disco disponível.

</dd> <dt>

<span id="memberOf"></span><span id="memberof"></span><span id="MEMBEROF"></span>[**memberOf**](/windows/desktop/ADSchema/a-memberof)
</dt> <dd>

O atributo [**memberOf**](/windows/desktop/ADSchema/a-memberof) é um atributo com vários valores que contém grupos dos quais o usuário é um membro direto, exceto para o grupo primário, que é representado pelo [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid). A associação de grupo depende do controlador de domínio (DC) do qual esse atributo é recuperado:

-   Em um DC para o domínio que contém o usuário, o [**membro**](/windows/desktop/ADSchema/a-memberof) do usuário é concluído em relação à associação de grupos nesse domínio; no entanto, **memberOf** não contém a associação do usuário em grupos locais e globais de domínio em outros domínios.
-   Em um servidor GC, o [**membro**](/windows/desktop/ADSchema/a-memberof) do usuário é concluído em relação a todas as associações de grupo universal.

Se ambas as condições forem verdadeiras para o DC, ambos os conjuntos de dados estarão contidos em [**memberOf**](/windows/desktop/ADSchema/a-memberof).

Lembre-se de que esse atributo lista os grupos que contêm o usuário em seu atributo de membro — ele não contém a lista recursiva de predecessores aninhados. Por exemplo, se O usuário O for um membro do grupo C e o grupo b e o grupo B tiverem sido aninhados no grupo A, o atributo [**memberOf**](/windows/desktop/ADSchema/a-memberof) do usuário o listará o grupo C e o grupo b, mas não o grupo a.

Esse atributo não é armazenado — é um atributo de back-link calculado.

</dd> <dt>

<span id="ntPwdHistory"></span><span id="ntpwdhistory"></span><span id="NTPWDHISTORY"></span>[**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory)
</dt> <dd>

o atributo [**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory) é o histórico de senha do usuário em Windows NT formato unidirecional (OWF). Windows 2000 usa o Windows NT OWF. Esse atributo é usado somente pelo sistema operacional. Esteja ciente de que você não pode derivar a senha de texto não criptografado do formulário OWF da senha.

</dd> <dt>

<span id="otherMailbox"></span><span id="othermailbox"></span><span id="OTHERMAILBOX"></span>[**otherMailbox**](/windows/desktop/ADSchema/a-othermailbox)
</dt> <dd>

O [**atributo otherMailbox**](/windows/desktop/ADSchema/a-othermailbox) é um atributo com vários valores que contém outros endereços de email adicionais em um formulário, por exemplo, "CCMAIL: JeffSmith".

</dd> <dt>

<span id="PasswordExpirationDate"></span><span id="passwordexpirationdate"></span><span id="PASSWORDEXPIRATIONDATE"></span>[**PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods)
</dt> <dd>

A data de expiração da senha não é um atributo no objeto de usuário. É um valor calculado com base na soma de [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) para o usuário e [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) do domínio do usuário. Para obter a data de validade da senha, obter a [**propriedade IADsUser.PasswordExpirationDate.**](/windows/desktop/ADSI/iadsuser-property-methods) Você não pode modificar esse atributo para um usuário; Em vez disso, de definir [**a propriedade IADsDomain.MaxPasswordAge**](/windows/desktop/ADSI/iadsdomain-property-methods) para alterar a configuração do domínio.

</dd> <dt>

<span id="primaryGroupID"></span><span id="primarygroupid"></span><span id="PRIMARYGROUPID"></span>[**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)
</dt> <dd>

O [**atributo primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) é um atributo de valor único que contém [**o primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) do grupo que é o grupo primário do objeto . O grupo primário do objeto não está incluído no [**atributo memberOf.**](/windows/desktop/ADSchema/a-memberof) Por exemplo, por padrão, o grupo principal de um objeto de usuário é **o primaryGroupToken** do grupo Usuários do Domínio, mas o grupo Usuários do Domínio não faz parte do atributo **memberOf** do objeto de usuário.

</dd> <dt>

<span id="profilePath"></span><span id="profilepath"></span><span id="PROFILEPATH"></span>[**profilePath**](/windows/desktop/ADSchema/a-profilepath)
</dt> <dd>

O [**atributo profilePath**](/windows/desktop/ADSchema/a-profilepath) especifica um caminho para o perfil do usuário. Esse valor pode ser uma cadeia de caracteres nula, um caminho absoluto local ou um caminho UNC.

</dd> <dt>

<span id="pwdLastSet"></span><span id="pwdlastset"></span><span id="PWDLASTSET"></span>[**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)
</dt> <dd>

O [**atributo pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) especifica quando a senha foi alterada pela última vez. Esse valor é armazenado como um inteiro grande que representa o número de intervalos de 100 nanossegundos desde 1º de janeiro de 1601 (UTC).

O sistema usa o valor desse atributo e o atributo [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) do domínio que contém o objeto de usuário para calcular a data de expiração da senha. Ou seja, a soma de [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) para o usuário e **maxPwdAge** do domínio do usuário.

Esse atributo controla se o usuário deve alterar a senha quando o usuário faz logo em seguida. Se [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) for zero, o padrão será que o usuário deverá alterar a senha no próximo logon. O valor -1 indica que o usuário não precisa alterar a senha no próximo logon. O sistema define esse valor como -1 depois que o usuário define a senha.

</dd> <dt>

<span id="sAMAccountType"></span><span id="samaccounttype"></span><span id="SAMACCOUNTTYPE"></span>[**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype)
</dt> <dd>

O [**atributo sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype) especifica um inteiro que representa o tipo de conta. Isso é definido pelo sistema operacional quando o objeto é criado.

</dd> <dt>

<span id="scriptPath"></span><span id="scriptpath"></span><span id="SCRIPTPATH"></span>[**Scriptpath**](/windows/desktop/ADSchema/a-scriptpath)
</dt> <dd>

O [**atributo scriptPath**](/windows/desktop/ADSchema/a-scriptpath) especifica o caminho do script de logon do usuário, .cmd, .exe ou .bat arquivo. A cadeia de caracteres pode ser nula.

</dd> <dt>

<span id="unicodePwd"></span><span id="unicodepwd"></span><span id="UNICODEPWD"></span>[**Unicodepwd**](/windows/desktop/ADSchema/a-unicodepwd)
</dt> <dd>

O [**atributo unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd) é a senha do usuário.

Para definir a senha do usuário, use o método [**IADsUser.ChangePassword,**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) se o script ou o aplicativo permitir que o usuário altere sua própria senha ou o método [**IADsUser.SetPassword,**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) se o script ou o aplicativo estiver permitindo que um administrador redefina uma senha.

A senha do usuário Windows NT formato único (OWF). Windows 2000 usa o Windows NT OWF. Esse atributo é usado apenas pelo sistema operacional. Esteja ciente de que você não pode derivar a senha de texto não criptografado do formulário OWF da senha.

</dd> <dt>

<span id="userAccountControl"></span><span id="useraccountcontrol"></span><span id="USERACCOUNTCONTROL"></span>[**Useraccountcontrol**](/windows/desktop/ADSchema/a-useraccountcontrol)
</dt> <dd>

O [**atributo userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) especifica sinalizadores que controlam senha, bloqueio, desabilitar/habilitar, script e comportamento de diretório home para o usuário. Esse atributo também contém um sinalizador que indica o tipo de conta do objeto . O objeto de usuário geralmente tem a CONTA NORMAL DE UF \_ \_ definida.

Os sinalizadores a seguir são definidos em Lmaccess.h.



| Sinalizador                     | Descrição                                                                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCRIPT DE UF \_               | O script de logon executado. Esse valor deve ser definido para LAN Manager 2.0 ou Windows NT.                                                                             |
| UF \_ ACCOUNTDISABLE       | A conta de usuário está desabilitada.                                                                                                                                    |
| UF \_ HOMEDIR \_ OBRIGATÓRIO    | O diretório home é necessário. Esse valor é ignorado em Windows NT e Windows 2000.                                                                            |
| UF \_ PASSWD \_ NOTREQD      | Nenhuma senha é necessária.                                                                                                                                         |
| A UNIVERSIDADE \_ PASSWD \_ NÃO PODE \_ MUDAR | O usuário não pode alterar a senha.                                                                                                                             |
| BLOQUEIO DE UF \_              | A conta está bloqueada no momento. Esse valor pode ser limpo para desbloquear uma conta bloqueada anteriormente. Esse valor não pode ser usado para bloquear uma conta bloqueada anteriormente. |
| A UNIVERSIDADE \_ NÃO \_ \_ EXPIRARÁ PASSWD | Representa a senha, que nunca deve expirar na conta.                                                                                               |



 

Os sinalizadores a seguir descrevem o tipo de conta. Somente um valor pode ser definido. Não é possível alterar o tipo de conta.



| Sinalizador                            | Descrição                                                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CONTA NORMAL DA UF \_ \_             | Esse é um tipo de conta padrão que representa um usuário típico.                                                                                                                                                                                  |
| CONTA \_ \_ DUPLICADA TEMP DA UF \_    | Essa é uma conta para usuários cuja conta primária está em outro domínio. Essa conta fornece acesso de usuário a esse domínio, mas não a nenhum domínio que confie nesse domínio. O Gerenciador de Usuários refere-se a esse tipo de conta como uma conta de usuário local. |
| CONTA CONFIÁVEL DA ESTAÇÃO \_ \_ DE TRABALHO \_ DA UF | Essa é uma conta de computador para uma estação de trabalho do Windows NT/Windows 2000 Professional ou Windows NT Server/Windows 2000 Server que seja membro desse domínio.                                                                                     |
| CONTA \_ DE CONFIANÇA DO \_ SERVIDOR \_ DA UNIVERSIDADE      | Essa é uma conta de computador para Windows NT controlador de domínio de backup que é membro desse domínio.                                                                                                                                           |
| CONTA \_ DE CONFIANÇA INTERDOMÍNIO \_ \_ DA UNIVERSIDADE | Essa é uma permissão para confiar em uma conta de Windows NT domínio que confia em outros domínios.                                                                                                                                                            |



 

</dd> <dt>

<span id="userCertificate"></span><span id="usercertificate"></span><span id="USERCERTIFICATE"></span>[**userCertificate**](/windows/desktop/ADSchema/a-usercertificate)
</dt> <dd>

O [**atributo userCertificate**](/windows/desktop/ADSchema/a-usercertificate) é um atributo com vários valores que contém os certificados X509v3 codificados em DER emitidos para o usuário. Esteja ciente de que esse atributo contém os certificados de chave pública emitidos para esse usuário pelo Serviço de Certificado da Microsoft.

</dd> <dt>

<span id="userSharedFolder"></span><span id="usersharedfolder"></span><span id="USERSHAREDFOLDER"></span>[**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder)
</dt> <dd>

O [**atributo userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder) especifica um caminho UNC para a pasta de documentos compartilhados do usuário. O caminho deve ser um caminho UNC de rede do diretório de \\ \\ compartilhamento do \\ servidor de \\ formulário. Esse valor pode ser uma cadeia de caracteres nula.

</dd> <dt>

<span id="userWorkstations"></span><span id="userworkstations"></span><span id="USERWORKSTATIONS"></span>[**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)
</dt> <dd>

O [**atributo userWorkstations**](/windows/desktop/ADSchema/a-userworkstations) é um atributo de valor único que contém os nomes NetBIOS das estações de trabalho nas quais o usuário pode fazer logoff. Cada nome NetBIOS é separado por uma vírgula.

Se nenhum valor for definido, isso indicará que não há restrição. Para desabilitar logons de todas as estações de trabalho para essa conta, de definir o valor DE \_ LMA ACCOUNTDISABLE (definido em Lmaccess.h) no [**atributo userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol)

</dd> </dl>

 

 
