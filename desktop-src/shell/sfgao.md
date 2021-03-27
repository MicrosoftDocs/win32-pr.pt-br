---
description: Atributos que podem ser recuperados em um item (arquivo ou pasta) ou conjunto de itens.
ms.assetid: 4cb85995-cdc8-4474-8c4d-c783ac91c759
title: SFGAO (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34f01691c3dbb1e5b76d93739b4893ffaf7c69e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662563"
---
# <a name="sfgao"></a>SFGAO

Atributos que podem ser recuperados em um item (arquivo ou pasta) ou conjunto de itens.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante/valor</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANCOPY"></span><span id="sfgao_cancopy"></span><dl> <dt><strong>SFGAO_CANCOPY</strong></dt> <dt>0x00000001</dt> </dl></td>
<td style="text-align: left;">Os itens especificados podem ser copiados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CANMOVE"></span><span id="sfgao_canmove"></span><dl> <dt><strong>SFGAO_CANMOVE</strong></dt> <dt>0x00000002</dt> </dl></td>
<td style="text-align: left;">Os itens especificados podem ser movidos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANLINK"></span><span id="sfgao_canlink"></span><dl> <dt><strong>SFGAO_CANLINK</strong></dt> <dt>0x00000004</dt> </dl></td>
<td style="text-align: left;">Os atalhos podem ser criados para os itens especificados. Esse atributo tem o mesmo valor que <a href="/windows/desktop/com/dropeffect-constants"><strong>DROPEFFECT_LINK</strong></a>. <br/> Se uma extensão de namespace retornar esse atributo, uma entrada <strong>criar atalho</strong> com um manipulador padrão será adicionada ao menu de atalho que é exibido durante as operações de arrastar e soltar. A extensão também pode implementar seu próprio manipulador para o verbo de <em>link</em> no lugar do padrão. Se a extensão for assim, será responsável pela criação do atalho.<br/> Um item de <strong>atalho criar</strong> também é adicionado ao menu <strong>arquivo</strong> do Windows Explorer e aos menus de atalho normais.<br/> Se o item for selecionado, o método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand"><strong>IContextMenu:: InvokeCommand</strong></a> do seu aplicativo será invocado com o membro <strong>LpVerb</strong> da estrutura <a href="/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-cminvokecommandinfo"><strong>CMINVOKECOMMANDINFO</strong></a> definida como <em>link</em>. Seu aplicativo é responsável por criar o link.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGE"></span><span id="sfgao_storage"></span><dl> <dt><strong>SFGAO_STORAGE</strong></dt> <dt>0x00000008</dt> </dl></td>
<td style="text-align: left;">Os itens especificados podem ser associados a um objeto <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a> por meio de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a>. Para obter mais informações sobre os recursos de manipulação de namespace, consulte <strong>IStorage</strong>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANRENAME"></span><span id="sfgao_canrename"></span><dl> <dt><strong>SFGAO_CANRENAME</strong></dt> <dt>0x00000010</dt> </dl></td>
<td style="text-align: left;">Os itens especificados podem ser renomeados. Observe que esse valor é essencialmente uma sugestão; Nem todos os clientes de namespace permitem que os itens sejam renomeados. No entanto, aqueles que devem ter esse atributo definido.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CANDELETE"></span><span id="sfgao_candelete"></span><dl> <dt><strong>SFGAO_CANDELETE</strong></dt> <dt>0x00000020</dt> </dl></td>
<td style="text-align: left;">Os itens especificados podem ser excluídos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HASPROPSHEET"></span><span id="sfgao_haspropsheet"></span><dl> <dt><strong>SFGAO_HASPROPSHEET</strong></dt> <dt>0x00000040</dt> </dl></td>
<td style="text-align: left;">Os itens especificados têm folhas de propriedades.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_DROPTARGET"></span><span id="sfgao_droptarget"></span><dl> <dt><strong>SFGAO_DROPTARGET</strong></dt> <dt>0x00000100</dt> </dl></td>
<td style="text-align: left;">Os itens especificados são drop targets.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CAPABILITYMASK"></span><span id="sfgao_capabilitymask"></span><dl> <dt><strong>SFGAO_CAPABILITYMASK</strong></dt> <dt>0x00000177</dt> </dl></td>
<td style="text-align: left;">Esse sinalizador é uma máscara para os atributos de funcionalidade: SFGAO_CANCOPY, SFGAO_CANMOVE, SFGAO_CANLINK, SFGAO_CANRENAME, SFGAO_CANDELETE, SFGAO_HASPROPSHEET e SFGAO_DROPTARGET. Os chamadores normalmente não usam esse valor.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_SYSTEM"></span><span id="sfgao_system"></span><dl> <dt><strong>SFGAO_SYSTEM</strong></dt> <dt>0x00001000</dt> </dl></td>
<td style="text-align: left;"><strong>Windows 7 e posterior</strong>. Os itens especificados são itens do sistema.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_ENCRYPTED"></span><span id="sfgao_encrypted"></span><dl> <dt><strong>SFGAO_ENCRYPTED</strong></dt> <dt>0x00002000</dt> </dl></td>
<td style="text-align: left;">Os itens especificados são criptografados e podem exigir apresentação especial.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_ISSLOW"></span><span id="sfgao_isslow"></span><dl> <dt><strong>SFGAO_ISSLOW</strong></dt> <dt>0x00004000</dt> </dl></td>
<td style="text-align: left;">Espera-se que o acesso ao item (por meio de <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> ou outras interfaces de armazenamento) seja uma operação lenta. Os aplicativos devem evitar o acesso a itens sinalizados com SFGAO_ISSLOW. <br/>
<blockquote>
[!Note]<br />
A abertura de um fluxo para um item geralmente é uma operação lenta em todos os momentos. SFGAO_ISSLOW indica que espera-se que seja especialmente lenta, por exemplo, no caso de conexões de rede lentas ou arquivos offline (FILE_ATTRIBUTE_OFFLINE). No entanto, consultar SFGAO_ISSLOW é uma operação lenta. Os aplicativos devem consultar SFGAO_ISSLOW apenas em um thread em segundo plano. Um método alternativo, como a recuperação da propriedade <a href="/windows/desktop/properties/props-system-fileattributes"><strong>PKEY_FileAttributes</strong></a> e o teste de FILE_ATTRIBUTE_OFFLINE, pode ser usado no lugar de uma chamada de método que envolve SFGAO_ISSLOW.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_GHOSTED"></span><span id="sfgao_ghosted"></span><dl> <dt><strong>SFGAO_GHOSTED</strong></dt> <dt>0x00008000</dt> </dl></td>
<td style="text-align: left;">Os itens especificados são mostrados como esmaecidos e não disponíveis para o usuário.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_LINK"></span><span id="sfgao_link"></span><dl> <dt><strong>SFGAO_LINK</strong></dt> <dt>0x00010000</dt> </dl></td>
<td style="text-align: left;">Os itens especificados são atalhos.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_SHARE"></span><span id="sfgao_share"></span><dl> <dt><strong>SFGAO_SHARE</strong></dt> <dt>0x00020000</dt> </dl></td>
<td style="text-align: left;">Os objetos especificados são compartilhados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_READONLY"></span><span id="sfgao_readonly"></span><dl> <dt><strong>SFGAO_READONLY</strong></dt> <dt>0x00040000</dt> </dl></td>
<td style="text-align: left;">Os itens especificados são somente leitura. No caso de pastas, isso significa que novos itens não podem ser criados nessas pastas. Isso não deve ser confundido com o comportamento especificado pelo sinalizador FILE_ATTRIBUTE_READONLY recuperado por <a href="/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata"><strong>IColumnProvider:: GetItemData</strong></a> em uma estrutura <a href="/windows/desktop/api/Shlobj/ns-shlobj-shcolumndata"><strong>SHCOLUMNDATA</strong></a> . FILE_ATTRIBUTE_READONLY não tem significado para as pastas do sistema de arquivos do Win32.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HIDDEN"></span><span id="sfgao_hidden"></span><dl> <dt><strong>SFGAO_HIDDEN</strong></dt> <dt>0x00080000</dt> </dl></td>
<td style="text-align: left;">O item ficará oculto e não deverá ser exibido, a menos que a opção <strong>mostrar pastas e arquivos ocultos</strong> esteja habilitada nas <strong>configurações de pasta</strong>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_DISPLAYATTRMASK"></span><span id="sfgao_displayattrmask"></span><dl> <dt><strong>SFGAO_DISPLAYATTRMASK</strong></dt> <dt>0x000FC000</dt> </dl></td>
<td style="text-align: left;">Não use.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_NONENUMERATED"></span><span id="sfgao_nonenumerated"></span><dl> <dt><strong>SFGAO_NONENUMERATED</strong></dt> <dt>0x00100000</dt> </dl></td>
<td style="text-align: left;">Os itens são itens não enumerados e devem estar ocultos. Eles não são retornados por meio de um enumerador, como aquele criado pelo método <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects"><strong>IShellFolder:: EnumObjects</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_NEWCONTENT"></span><span id="sfgao_newcontent"></span><dl> <dt><strong>SFGAO_NEWCONTENT</strong></dt> <dt>0x00200000</dt> </dl></td>
<td style="text-align: left;">Os itens contêm novo conteúdo, conforme definido pelo aplicativo específico.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_CANMONIKER"></span><span id="sfgao_canmoniker"></span><dl> <dt><strong>SFGAO_CANMONIKER</strong></dt> </dl></td>
<td style="text-align: left;">Não há suporte.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_HASSTORAGE"></span><span id="sfgao_hasstorage"></span><dl> <dt><strong>SFGAO_HASSTORAGE</strong></dt> </dl></td>
<td style="text-align: left;">Não há suporte.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_STREAM"></span><span id="sfgao_stream"></span><dl> <dt><strong>SFGAO_STREAM</strong></dt> <dt>0x00400000</dt> </dl></td>
<td style="text-align: left;">Indica que o item tem um fluxo associado a ele. Esse fluxo pode ser acessado por meio de uma chamada para <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject"><strong>IShellFolder:: BindToObject</strong></a> ou <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-bindtohandler"><strong>IShellItem:: BindToHandler</strong></a> com IID_IStream no parâmetro <em>riid</em> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGEANCESTOR"></span><span id="sfgao_storageancestor"></span><dl> <dt><strong>SFGAO_STORAGEANCESTOR</strong></dt> <dt>0x00800000</dt> </dl></td>
<td style="text-align: left;">Os filhos deste item estão acessíveis por meio de <a href="/windows/desktop/api/objidl/nn-objidl-istream"><strong>IStream</strong></a> ou <a href="/windows/desktop/api/objidl/nn-objidl-istorage"><strong>IStorage</strong></a>. Esses filhos são sinalizados com SFGAO_STORAGE ou SFGAO_STREAM.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_VALIDATE"></span><span id="sfgao_validate"></span><dl> <dt><strong>SFGAO_VALIDATE</strong></dt> <dt>0x01000000</dt> </dl></td>
<td style="text-align: left;">Quando especificado como entrada, SFGAO_VALIDATE instrui a pasta para validar que os itens contidos em uma pasta ou matriz de item de shell existam. Se um ou mais desses itens não existirem, <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof"><strong>IShellFolder:: GetAttributesOf</strong></a> e <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes"><strong>IShellitemArray:: GetAttributes</strong></a> retornarão um código de falha. Esse sinalizador nunca é retornado como um valor [out].<br/> Quando usado com a pasta do sistema de arquivos, SFGAO_VALIDATE instrui a pasta a descartar as propriedades armazenadas em cache recuperadas por clientes de <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsex"><strong>IShellFolder2:: GetDetailsEx</strong></a> que podem ter acumulado para os itens especificados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_REMOVABLE"></span><span id="sfgao_removable"></span><dl> <dt><strong>SFGAO_REMOVABLE</strong></dt> <dt>0x02000000</dt> </dl></td>
<td style="text-align: left;">Os itens especificados estão em mídia removível ou são dispositivos removíveis.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_COMPRESSED"></span><span id="sfgao_compressed"></span><dl> <dt><strong>SFGAO_COMPRESSED</strong></dt> <dt>0x04000000</dt> </dl></td>
<td style="text-align: left;">Os itens especificados são compactados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_BROWSABLE"></span><span id="sfgao_browsable"></span><dl> <dt><strong>SFGAO_BROWSABLE</strong></dt> <dt>0x08000000</dt> </dl></td>
<td style="text-align: left;">Os itens especificados podem ser hospedados dentro de um navegador da Web ou de um quadro do Windows Explorer.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_FILESYSANCESTOR"></span><span id="sfgao_filesysancestor"></span><dl> <dt><strong>SFGAO_FILESYSANCESTOR</strong></dt> <dt>0x10000000</dt> </dl></td>
<td style="text-align: left;">As pastas especificadas são pastas do sistema de arquivos ou contêm pelo menos um descendente (filho, neto ou posterior) que é uma pasta do sistema de arquivos (SFGAO_FILESYSTEM).<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_FOLDER"></span><span id="sfgao_folder"></span><dl> <dt><strong>SFGAO_FOLDER</strong></dt> <dt>0x20000000</dt> </dl></td>
<td style="text-align: left;">Os itens especificados são pastas. Alguns itens podem ser sinalizados com SFGAO_STREAM e SFGAO_FOLDER, como um arquivo compactado com uma extensão de nome de arquivo. zip. Alguns aplicativos podem incluir esse sinalizador ao testar itens que são arquivos e contêineres.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_FILESYSTEM"></span><span id="sfgao_filesystem"></span><dl> <dt><strong>SFGAO_FILESYSTEM</strong></dt> <dt>0x40000000</dt> </dl></td>
<td style="text-align: left;">As pastas ou os arquivos especificados fazem parte do sistema de arquivos (ou seja, arquivos, diretórios ou diretórios raiz). Os nomes analisados dos itens podem ser considerados como caminhos válidos do sistema de arquivos do Win32. Esses caminhos podem ser baseados em letra UNC ou unidade.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_STORAGECAPMASK"></span><span id="sfgao_storagecapmask"></span><dl> <dt><strong>SFGAO_STORAGECAPMASK</strong></dt> <dt>0x70C50008</dt> </dl></td>
<td style="text-align: left;">Esse sinalizador é uma máscara para os atributos de funcionalidade de armazenamento: SFGAO_STORAGE, SFGAO_LINK, SFGAO_READONLY, SFGAO_STREAM, SFGAO_STORAGEANCESTOR, SFGAO_FILESYSANCESTOR, SFGAO_FOLDER e SFGAO_FILESYSTEM. Os chamadores normalmente não usam esse valor.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_HASSUBFOLDER"></span><span id="sfgao_hassubfolder"></span><dl> <dt><strong>SFGAO_HASSUBFOLDER</strong></dt> <dt>0x80000000</dt> </dl></td>
<td style="text-align: left;">As pastas especificadas têm subpastas. O atributo SFGAO_HASSUBFOLDER é apenas consultoria e pode ser retornado por implementações de pastas do Shell, mesmo que eles não contenham subpastas. Observe, no entanto, que o inverso — falha ao retornar SFGAO_HASSUBFOLDER — afirma definiamente que os objetos de pasta não têm subpastas.<br/> O retorno de SFGAO_HASSUBFOLDER é recomendado sempre que uma quantidade significativa de tempo é necessária para determinar se existem subpastas. Por exemplo, o shell sempre retorna SFGAO_HASSUBFOLDER quando uma pasta está localizada em uma unidade de rede.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="SFGAO_CONTENTSMASK"></span><span id="sfgao_contentsmask"></span><dl> <dt><strong>SFGAO_CONTENTSMASK</strong></dt> <dt>0x80000000</dt> </dl></td>
<td style="text-align: left;">Este sinalizador é uma máscara para atributos de conteúdo, no momento, somente SFGAO_HASSUBFOLDER. Os chamadores normalmente não usam esse valor.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="SFGAO_PKEYSFGAOMASK"></span><span id="sfgao_pkeysfgaomask"></span><dl> <dt><strong>SFGAO_PKEYSFGAOMASK</strong></dt> <dt>0x81044000</dt> </dl></td>
<td style="text-align: left;">Máscara usada pela propriedade <a href="/windows/desktop/properties/props-system-sfgaoflags">PKEY_SFGAOFlags</a> para determinar atributos que são considerados para causar cálculos lentos ou ausência de contexto: SFGAO_ISSLOW, SFGAO_READONLY, SFGAO_HASSUBFOLDER e SFGAO_VALIDATE. Os chamadores normalmente não usam esse valor.<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IShellFolder::GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof)
</dt> <dt>

[**IShellFolder::P arseDisplayName**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname)
</dt> <dt>

[**IShellItemArray:: GetAttributes**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitemarray-getattributes)
</dt> </dl>

 

 
